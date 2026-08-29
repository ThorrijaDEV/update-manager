# Update Manager — Advanced Arch/AUR Update Tool

A terminal-based interactive update manager for Omarchy and Arch Linux, providing a clean interface for managing system and AUR updates with safety features.

## What is it?

A Python TUI application that wraps pacman and your AUR helper (yay, paru, etc.) to provide an interactive update experience: see what's updating, read changelogs, select packages, and track progress — with automatic snapshots via omarchy-update hooks.

## What does it do?

- **List available updates** from official repositories and AUR in one view
- **Selective package updates**: choose which packages to update (space to toggle, `a` for all)
- **View changelogs and release notes** for each package before updating
- **Progress display** during download and installation with real-time output
- **Integration with omarchy-update**: automatic pre-update snapshots and post-update hooks
- **View update logs** from previous runs
- **Customizable options**: skip certain packages, hold packages, configure AUR helper
- **Keyboard-driven TUI**: vim-like navigation, no mouse required

## Technologies

Python 3.x, pacman, yay/paru (AUR helper), psutil (optional, for system monitoring)

## Installation

### Dependencies

- Python 3.x
- pacman (system package manager)
- yay or your preferred AUR helper
- psutil (for system monitoring, optional but recommended)

### Install from source

```bash
git clone https://github.com/ThorrijaDEV/update-manager
cd update-manager
make install
```

## Usage

Run the update manager:

```bash
sudo update-manager
```

Note: Running with sudo is required for system updates.

## Configuration

The update manager can be configured by editing `config.json` in the installation directory. Options include:
- AUR helper command (yay, paru, etc.)
- Packages to hold/skip
- Snapshot behavior
- UI preferences

## Status

**Functional / Maintenance**

Core features working: update listing, selection, changelog viewing, progress display, omarchy integration, logging. Used daily on Omarchy systems.

## Repository Note

This repository contains documentation only. The implementation is private code.

## License

MIT