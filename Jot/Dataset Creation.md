
## Machines

- 2 lab machines, 50GB VRAM each
- 4 Azure compute instances, 16GB VRAM each

## Queries Being Used

1. For `Handwritten English` identifiers:
```
mediatype:(texts) and language:(Handwritten English)
```
- Running on `Gizmo` machine

2. For `Latin` identifiers:
```
mediatype:(texts) and language:(Latin)
```
- Running on `Gremlin` machine

4. For `Office Document` identifiers:
```
mediatype:(texts) and collection:(nationalsecurityarchive)
```
- This proces