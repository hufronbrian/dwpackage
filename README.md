# dwpackage

Cross-platform script installer template for Python-based CLI tools.

No package manager needed - just PowerShell (Windows) and Bash (Linux/Mac/WSL).

## Features

- Dependency checking with optional auto-install
- Clean update (stops services, removes old files, copies new)
- PATH management (add on install, remove on uninstall)
- Service/daemon management (stop before update, notify to restart)
- Non-interactive mode (-y flag)
- Cross-platform (Windows + Linux/Mac/WSL)

## Usage

1. Copy template files to your project
2. Edit paths and dependencies for your tool
3. Run `./install.ps1` (Windows) or `./install.sh` (Linux)

## File Structure

```
your-project/
  install.ps1       # Windows installer
  install.sh        # Linux/Mac/WSL installer
  uninstall.ps1     # Windows uninstaller
  uninstall.sh      # Linux/Mac/WSL uninstaller
  win/              # Windows source files
  unx/              # Linux/Mac/WSL source files
  docs/
    install.txt     # Install behavior documentation
    uninstall.txt   # Uninstall behavior documentation
```

## Install Locations

- Windows: `C:\Users\{user}\bin\{toolname}\`
- Linux: `~/.local/bin/{toolname}/`

## Documentation

- [docs/install.txt](docs/install.txt) - Install behavior and patterns
- [docs/uninstall.txt](docs/uninstall.txt) - Uninstall behavior and patterns
- [docs/dwml-registry.txt](docs/dwml-registry.txt) - DWML format for service registries

## Based On

Patterns extracted from [DocWire](https://github.com/hufronbrian/docwire) installer.
