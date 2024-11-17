# Obsidian Git Auto-Sync

Automatically sync your Obsidian vault to GitHub every minute when changes are detected. This solution is designed for Linux systems and uses systemd for service management.

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
        
        # Setup logging
        logging.basicConfig(
            filename='obsidian_sync.log',
            level=logging.INFO,
            format='%(asctime)s - %(message)s'
        )
        
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
            
            # Get current datetime for commit message
            commit_date = datetime.now().strftime("%Y-%m-%d %H:%M:%S")
            
            # Run git commands
            subprocess.run(['git', 'add', '.'], check=True)
            subprocess.run(['git', 'commit', '-m', f'Auto-sync: {commit_date}'], check=True)
            subprocess.run(['git', 'pull', '--rebase'], check=True)
            subprocess.run(['git', 'push'], check=True)
            
            logging.info(f'Successfully synced vault at {commit_date}')
            
        except subprocess.CalledProcessError as e:
            logging.error(f'Git operation failed: {str(e)}')
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
    # Replace with your vault path
    VAULT_PATH = "/path/to/your/obsidian/vault"
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