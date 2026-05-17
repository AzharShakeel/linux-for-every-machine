# 🌿 Linux Mint — Distro Guide

> *The most Windows-like Linux experience. The single best recommendation for anyone switching from Windows.*

---

## 📋 Quick Summary

| Property | Details |
|----------|---------|
| 🏷️ Based on | Ubuntu LTS |
| 🎯 Primary use | Daily desktop, Windows replacement |
| 💾 Minimum RAM | 2 GB (4 GB recommended) |
| 💿 Minimum storage | 20 GB |
| 👤 Target user | Absolute beginners, Windows switchers |
| 🌐 Official site | [linuxmint.com](https://linuxmint.com) |

---

## ✅ When to Use Linux Mint

- You are **switching from Windows** and want the most familiar experience
- You want a **stable, beginner-friendly** daily desktop
- You want a system that **just works** — drivers, codecs, software all included
- You want **long-term stability** — Mint is based on Ubuntu LTS (2 years of support)
- You don't want to touch the terminal unless you choose to

## ❌ When NOT to Use Linux Mint

- You need **cutting-edge software** — Mint prioritizes stability over latest versions
- You want the **latest kernel** by default — not Mint's priority
- You need a **server OS** — use Debian or Ubuntu Server instead

---

## 💻 Hardware Requirements

| Spec | Minimum | Recommended |
|------|---------|-------------|
| 🖥️ CPU | 64-bit dual-core | 64-bit quad-core |
| 🧠 RAM | 2 GB | 4 GB+ |
| 💾 Storage | 20 GB | 50 GB+ |
| 🖥️ Display | 1024×768 | 1920×1080 |

---

## 🎨 Which Desktop Edition

| Edition | Desktop | RAM Usage | Best For |
|---------|---------|-----------|---------|
| 🌟 **Cinnamon** | Windows-like | ~700 MB | Most users — default recommendation |
| 🌀 **MATE** | Classic, efficient | ~500 MB | Older hardware with enough RAM |
| ❄️ **XFCE** | Lightweight | ~400 MB | Low-RAM machines, speed priority |

**Pick Cinnamon** unless you have less than 4 GB RAM — it's the most polished experience.

---

## 📥 Download

1. Go to **[linuxmint.com/download.php](https://linuxmint.com/download.php)**
2. Select **Cinnamon** edition (recommended)
3. Download the **64-bit ISO**
4. Verify the SHA256 checksum

---

## 🔧 Install

```bash
# Flash to USB on Linux
sudo dd if=linuxmint-*.iso of=/dev/sdX bs=4M status=progress && sync
```

1. Boot from USB
2. Double-click **Install Linux Mint** on the desktop
3. Choose language, keyboard, timezone
4. ✅ Check **"Install third-party software"** — important for codecs and drivers
5. Choose **Erase disk and install Linux Mint** for a clean install
6. Create user and password
7. Reboot and remove USB

---

## ⚡ Post-Install Commands

```bash
# Update system fully
sudo apt update && sudo apt upgrade -y

# Install common essentials
sudo apt install -y curl git wget htop neofetch build-essential

# Install VS Code
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -o root -g root -m 644 packages.microsoft.gpg /usr/share/keyrings/
sudo sh -c 'echo "deb [arch=amd64 signed-by=/usr/share/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'
sudo apt update && sudo apt install -y code
```

---

## 🛠️ First Things to Do After Install

1. 🔄 Run **Update Manager** → install all updates
2. 🖥️ Go to **Driver Manager** → install proprietary GPU/WiFi drivers if needed
3. 🎨 Customize the desktop in **System Settings**
4. 📦 Open **Software Manager** to install apps graphically
5. 🔐 Set up **Timeshift** (pre-installed) for system snapshots

---

## 💡 Tips

- Mint ships with **VLC, LibreOffice, Thunderbird** already — you're ready to work immediately
- Use **Timeshift** — it's the best Linux system-restore tool and comes pre-installed
- The **Software Manager** is your app store — no terminal needed for most installs

---

## 🔗 Resources

- 📖 [Linux Mint User Guide](https://linuxmint.com/documentation.php)
- 📋 Related playbook: [`playbooks/02-from-windows-to-linux-desktop.md`](../playbooks/02-from-windows-to-linux-desktop.md)

---

*Part of [linux-for-every-machine](../README.md) · Copyright © 2026 Azhar Shakeel*
