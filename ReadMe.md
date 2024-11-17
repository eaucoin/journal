# My Obsidian Journal, Synced With GitHub

This is my personal journal. Below, I've included some documentation for how I sync this journal with this repository, which anyone may use.

## Prerequisites

- Linux operating system
- Python 3.6 or higher
- Git installed and configured
- GitHub account
- Obsidian vault initialized as a Git repository

## Installation

### 1. Install Required Python Package

```bash
pip3 install watchdog
```

### 2. Create the Sync Script

Create a new file called `obsidian_sync.py` and add the following code:

```python
import os
import time
import subprocess
from datetime import datetime
from watchdog.observers import Observer
from watchdog.events import FileSystemEventHandler
import logging

class ObsidianVaultHandler(FileSystemEventHandler):
    def __init__(self, vault_path):
        self.vault_path = vault_path
        self.last_sync = 0
        self.sync_cooldown = 60  # 1 minute cooldown
        self.branch_name = None
        
        # Setup logging
        logging.basicConfig(
            filename='obsidian_sync.log',
            level=logging.INFO,
            format='%(asctime)s - %(message)s'
        )
        
        # Initialize git configuration
        self.setup_git()
        
    def get_branch_name(self):
        """Get current branch name"""
        result = subprocess.run(['git', 'rev-parse', '--abbrev-ref', 'HEAD'],
                              check=True, capture_output=True, text=True)
        return result.stdout.strip()
        
    def setup_git(self):
        """Ensure git repository is properly configured"""
        try:
            os.chdir(self.vault_path)
            
            # Get current branch name
            self.branch_name = self.get_branch_name()
            logging.info(f"Current branch: {self.branch_name}")
            
            # Check if remote exists and get its URL
            try:
                remote_url = subprocess.run(['git', 'remote', 'get-url', 'origin'], 
                                         check=True, capture_output=True, text=True)
                logging.info(f"Remote URL: {remote_url.stdout.strip()}")
            except subprocess.CalledProcessError:
                logging.error("No remote 'origin' found. Please set up remote repository first")
                raise ValueError("Git remote not configured")
            
            # Fetch from remote to ensure we have the latest refs
            subprocess.run(['git', 'fetch', 'origin'], check=True, capture_output=True)
            
            # Setup tracking
            try:
                subprocess.run(['git', 'branch', f'--set-upstream-to=origin/{self.branch_name}', self.branch_name],
                             check=True, capture_output=True)
                logging.info(f"Set up tracking for branch {self.branch_name}")
            except subprocess.CalledProcessError:
                # If tracking already exists, this is fine
                pass
                
            # Test push access
            try:
                subprocess.run(['git', 'push', '--dry-run'], check=True, capture_output=True)
            except subprocess.CalledProcessError:
                logging.error("Unable to push to remote. Please check your Git credentials")
                raise ValueError("Git push access not configured")
                
            logging.info("Git repository successfully configured")
            
        except Exception as e:
            logging.error(f"Git setup failed: {str(e)}")
            raise
        
    def on_modified(self, event):
        if event.is_directory:
            return
            
        # Only process markdown files
        if not event.src_path.endswith('.md'):
            return
            
        current_time = time.time()
        if current_time - self.last_sync >= self.sync_cooldown:
            self.sync_vault()
            self.last_sync = current_time

    def sync_vault(self):
        try:
            os.chdir(self.vault_path)
            
            # Check if there are changes to commit
            status = subprocess.run(['git', 'status', '--porcelain'], 
                                 capture_output=True, text=True).stdout.strip()
            
            if not status:
                logging.info("No changes to sync")
                return
                
            # Get current datetime for commit message
            commit_date = datetime.now().strftime("%Y-%m-%d %H:%M:%S")
            
            # Run git commands with proper error handling
            try:
                # Stage changes
                subprocess.run(['git', 'add', '.'], check=True, capture_output=True)
                
                # Commit changes
                subprocess.run(['git', 'commit', '-m', f'Auto-sync: {commit_date}'],
                             check=True, capture_output=True)
                
                # Fetch latest changes
                subprocess.run(['git', 'fetch', 'origin'], check=True, capture_output=True)
                
                # Rebase against the remote branch
                try:
                    subprocess.run(['git', 'rebase', f'origin/{self.branch_name}'],
                                 check=True, capture_output=True)
                except subprocess.CalledProcessError as e:
                    logging.error(f"Rebase failed: {e.stderr}")
                    subprocess.run(['git', 'rebase', '--abort'], capture_output=True)
                    # Try a simple pull instead
                    subprocess.run(['git', 'pull', '--ff-only'], check=True, capture_output=True)
                
                # Push changes
                subprocess.run(['git', 'push', 'origin', self.branch_name],
                             check=True, capture_output=True)
                
                logging.info(f'Successfully synced vault at {commit_date}')
                
            except subprocess.CalledProcessError as e:
                logging.error(f'Git operation failed: {e.stderr}')
                raise
                
        except Exception as e:
            logging.error(f'Unexpected error during sync: {str(e)}')

def start_vault_sync(vault_path):
    # Verify vault path exists
    if not os.path.exists(vault_path):
        raise ValueError(f"Vault path does not exist: {vault_path}")
        
    # Verify it's a git repository
    git_path = os.path.join(vault_path, '.git')
    if not os.path.exists(git_path):
        raise ValueError(f"No Git repository found in: {vault_path}")
    
    # Setup the file system observer
    event_handler = ObsidianVaultHandler(vault_path)
    observer = Observer()
    observer.schedule(event_handler, vault_path, recursive=True)
    
    print(f"Starting Obsidian vault sync for: {vault_path}")
    print("Press Ctrl+C to stop")
    
    observer.start()
    try:
        while True:
            time.sleep(1)
    except KeyboardInterrupt:
        observer.stop()
        print("\nStopping vault sync...")
    observer.join()

if __name__ == "__main__":
    VAULT_PATH = "/your/vault/path"  # Your vault path
    start_vault_sync(VAULT_PATH)
```

### 3. Configure the Script

1. Edit the `obsidian_sync.py` file
2. Replace `VAULT_PATH` with the actual path to your Obsidian vault
3. Make the script executable:
```bash
chmod +x /path/to/obsidian_sync.py
```

### 4. Create Systemd Service

1. Create a new service file:
```bash
sudo nano /etc/systemd/system/obsidian-sync.service
```

2. Add the following content:
```ini
[Unit]
Description=Obsidian Git Sync Service
After=network.target

[Service]
Type=simple
User=YOUR_USERNAME
ExecStart=/usr/bin/python3 /path/to/obsidian_sync.py
WorkingDirectory=/path/to/obsidian/vault
Restart=always
RestartSec=10
Environment=PYTHONUNBUFFERED=1

[Install]
WantedBy=multi-user.target
```

3. Replace:
   - `YOUR_USERNAME` with your Linux username
   - `/path/to/obsidian_sync.py` with the actual path to your script
   - `/path/to/obsidian/vault` with your vault path

### 5. Enable and Start the Service

```bash
# Reload systemd daemon
sudo systemctl daemon-reload

# Enable the service to start on boot
sudo systemctl enable obsidian-sync

# Start the service
sudo systemctl start obsidian-sync
```

### 6. Verify Installation

1. Check service status:
```bash
sudo systemctl status obsidian-sync
```

2. Check logs:
```bash
# View service logs
journalctl -u obsidian-sync

# View sync logs
tail -f /path/to/obsidian/vault/obsidian_sync.log
```

## Usage

Once installed and running, the service will:
- Monitor your Obsidian vault for changes to markdown files
- Commit and push changes to GitHub every minute if modifications are detected
- Handle merge conflicts through rebase
- Log all sync activities

The service runs automatically on system startup and continues running until the system is shut down.

## Troubleshooting

### Git Authentication

1. Ensure your Git credentials are properly configured:
```bash
git config --global credential.helper store
```

2. Make a manual push to store credentials:
```bash
cd /path/to/obsidian/vault
git push
```

### Common Issues

1. **Service won't start:**
   - Check logs: `journalctl -u obsidian-sync`
   - Verify paths in service file
   - Ensure proper permissions

2. **Changes not syncing:**
   - Verify Git repository status
   - Check `obsidian_sync.log`
   - Ensure network connectivity

3. **Permission errors:**
   - Verify file ownership
   - Check service user configuration

## License

MIT License

## Contributing

Feel free to submit issues and pull requests.

## Support

Create an issue in the GitHub repository for support requests.