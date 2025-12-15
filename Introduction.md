## What is dcli?
`dcli` is an open-source command-line utility created by [_TheBlackDon_](https://gitlab.com/theblackdon) and hosted on GitLab that aims to bring **declarative configuration and modular package management** to _[Arch Linux](https://archlinux.org/)_ systems. It takes inspiration from tools like [_NixOS_](nixos.org) by allowing users to specify packages and system state in configuration files (previously JSON, presently YAML), and then automatically apply those configurations to the system via CLI commands such as `dcli sync` and `dcli install` — similar to how declarative package management works in functional OS tools.

### Features of dcli
- **Interactive TUI Interface**: Beautiful fzf-powered interfaces for package search, module management, snapshots, and hooks
- **Declarative Package Management**: Define your packages in YAML files and sync your system to match
- **Flexible Configuration Structure**: Choose between simple single-file or advanced multi-machine setups with imports
- **Config Migration Tool**: Safely migrate from old structure to new clean layout with `dcli migrate`
- **Flatpak Support**: Seamlessly manage flatpak applications alongside pacman packages
- **Module System**: Organize packages into reusable modules (gaming, development, etc.)
- **Host-Specific Configurations**: Maintain different package sets per machine with full config imports
- **Automatic Backups**: Integrates with Timeshift/Snapper for automatic snapshots before changes (skip with `--no-backup`)
- **Conflict Detection**: Prevents enabling conflicting modules
- **Post-Install Hooks**: Run scripts after package installation (skip with `--no-hooks`)
- **Safe Package Merge**: Capture manually installed packages to separate file (explicit packages only, never dependencies)
- **Git Repository Management**: Built-in commands to sync configurations across machines
- **Self-Updating**: Update dcli itself with a single command
- **Package Management Shortcuts**: Quick wrappers around pacman and [AUR](https://aur.archlinux.org/) helpers
- **Zero Runtime Dependencies**: Self-contained Rust binary with no external dependencies required

### TUI Interface Features
- Consistent blue borders with cyan labels
- TAB for multi-select (where applicable)
- Real-time search/filtering
- Live preview panes
- Keyboard-driven workflow

*For installing the dcli tool, steps are mentioned in [[Installation]] page.*
