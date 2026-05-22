# Linux Gamer Life openSUSE KDE Bootstrap

This script converts a minimal openSUSE Server installation into a complete Linux Gamer Life desktop environment with KDE Plasma, gaming tools, multimedia support, virtualization, and development utilities.

It is designed to be run once from TTY after installing openSUSE using the net installer.

---

## Overview

Starting point:

- openSUSE installed using the **Net Installer**
- **Server pattern selected**
- Booted into **TTY (no desktop environment)**

End result after running the script:

- KDE Plasma desktop with SDDM
- Gaming tools including Steam, Lutris, MangoHud, OBS Studio
- Full multimedia support with codecs and FFmpeg
- Flatpak with Flathub configured
- Virtualization stack with virt-manager and libvirt
- Python development tools with pipx, yt-dlp, and tldr
- AMD Mesa, Vulkan, and VA-API support
- Linux Gamer Life standard desktop environment

---

## Install openSUSE (Server)

Download the openSUSE Net Installer from the official site:

https://www.opensuse.org/

During installation:

- Select **Server** when choosing system role
- Complete installation normally
- Reboot into your new system

You will be presented with a TTY login prompt.

---

## Run the Bootstrap Script

Log in, then run:

```bash
curl -fsSL https://tinyurl.com/lgl-opensuse-kde | sudo bash
```

This will:

- Detect your openSUSE version (Leap or Tumbleweed)
- Configure required repositories
- Install KDE Plasma
- Install gaming tools
- Install codecs and multimedia support
- Install virtualization tools
- Configure Flatpak and essential applications
- Set KDE as the default boot target

When complete, reboot:

```bash
reboot
```

---

## What Gets Installed

### Desktop Environment

- KDE Plasma
- SDDM display manager
- Konsole
- Spectacle
- Ark
- Okular
- Gwenview
- KDE Discover

---

### Gaming Tools

- Steam
- Lutris
- MangoHud
- OBS Studio
- ProtonUp-Qt (Flatpak)
- ProtonPlus (Flatpak)
- Heroic Games Launcher (Flatpak)

---

### Multimedia Support

Configured via repository:

- FFmpeg
- GStreamer plugins (base, good, bad, ugly, libav)
- VLC

Provides full codec support for media playback and recording.

---

### Graphics Stack (AMD)

Installs:

- Mesa
- Mesa Vulkan drivers
- Vulkan tools
- VA-API support
- AMD Vulkan ICD

Optimized for AMD GPUs.

---

### Flatpak Support

Installs and configures:

- Flatpak
- Flathub repository

Installs:

- Flatseal
- ProtonUp-Qt
- ProtonPlus
- Heroic Launcher
- LibreOffice

---

### Virtualization

Installs full virtualization stack:

- virt-manager
- QEMU
- libvirt
- virt-install
- virt-viewer
- OVMF
- swtpm

Enables libvirt and adds your user to required groups.

---

### Development Tools

Installs:

- Python 3
- pip
- pipx
- virtualenv

Installs via pipx:

- yt-dlp
- tldr

Configured for the normal user, not root.

---

### System Configuration

Sets:

- KDE Plasma as default desktop
- SDDM as display manager
- Graphical boot target

---

## Supported openSUSE Versions

- openSUSE Tumbleweed
- openSUSE Leap

Script automatically detects version and configures repositories correctly.

---

## Safe to Re-Run

The script is designed to be safe if run again.

It will:

- Skip already installed packages
- Skip existing repositories
- Only install missing components

---

## Intended Use

This script is part of the Linux Gamer Life environment and is designed to provide a consistent openSUSE setup for:

- Gaming
- Content creation
- Virtualization
- Development
- Daily desktop use

---

## Notes

This script does not perform a full system upgrade. It installs only what is required.

Reboot after completion to start KDE Plasma.

---

## Linux Gamer Life

Part of the Linux Gamer Life ecosystem.

https://github.com/linuxgamerlife
