#### Prerequisites
- Arch Linux or an Arch Linux based distro (e.g. CachyOS, EndeavourOS, etc)
- Rust tool-chain (cargo) - required for building/updating the package, not for runtime

#### Optional Packages (Recommended)
- An AUR helper for package support (e.g. `paru`, `yay`, etc)
- Rollback/snapshot functionality packages (e.g. `timeshift` or `snapper`)
- `fzf` for TUI features and quick file management utility.

*Note: If Rust tool-chain is not present in the system, then the install script will automatically install it and build the package.*

*Otherwise it can be manually installed from [here](curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh)*

### Procedure
```bash
git clone https://gitlab.com/theblackdon/dcli.git
cd dcli
./install.sh
```

The installer will: 
1. Check for Rust and offer to install it automatically if not found
2. Build the Rust binary with `cargo build --release` (if not already built)
3. Copy the binary to `/usr/local/bin/dcli` (requires admin privileges)
4. Set executable permissions
5. Verify the installation
6. Check for optional dependencies (AUR helper, backup tools)