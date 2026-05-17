# 🪶 Linux Lite — Distro Guide

> *The most beginner-friendly lightweight Linux. If you have an old laptop and have never used Linux before, start here.*

---

## 📋 Quick Summary

| Property | Details |
|----------|---------|
| 🏷️ Based on | Ubuntu LTS |
| 🎯 Primary use | Old/low-end hardware, Windows replacement |
| 💾 Minimum RAM | 768 MB (1 GB recommended) |
| 💿 Minimum storage | 8 GB |
| 👤 Target user | Absolute beginners with old hardware |
| 🌐 Official site | [linuxliteos.com](https://www.linuxliteos.com) |

---

## ✅ When to Use Linux Lite

- You have an **old laptop with 1–2 GB RAM** and want it usable again
- You are a **complete beginner** to Linux — Linux Lite is the gentlest entry point
- You want a **Windows XP/7-era feel** — familiar taskbar, Start menu equivalent
- You want **long-term stability** — based on Ubuntu LTS with 5 years support
- You need a system that **runs fast on weak hardware**

## ❌ When NOT to Use Linux Lite

- You have **4+ GB RAM** — use Linux Mint Cinnamon instead for a better experience
- You need **cutting-edge software** — Lite's Ubuntu LTS base is stable, not bleeding-edge
- You want **advanced customization** — MX Linux gives more control at similar weight

---

## 💻 Hardware Requirements

| Spec | Minimum | Recommended |
|------|---------|-------------|
| 🖥️ CPU | 64-bit (32-bit also supported on older versions) | 64-bit dual-core |
| 🧠 RAM | 768 MB | 1 GB+ |
| 💾 Storage | 8 GB | 20 GB+ |
| 🖥️ Display | 1024×768 | 1366×768+ |

> 💡 Linux Lite is one of the few distros that genuinely works well at 1 GB RAM.

---

## 📥 Download

1. Go to **[linuxliteos.com/download.php](https://www.linuxliteos.com/download.php)**
2. Download the **64-bit ISO** (32-bit available for very old CPUs)
3. Flash with Rufus (Windows) or `dd` (Linux)

---

## 🔧 Install

```bash
# Flash to USB on Linux
sudo dd if=linux-lite-*.iso of=/dev/sdX bs=4M status=progress && sync
```

1. Boot from USB
2. Double-click **Install Linux Lite** on the desktop
3. Choose language, keyboard, timezone
4. ✅ Check **"Install third-party software"** — codecs and drivers
5. Select **Erase disk and install**
6. Create user and strong password
7. Reboot

---

## ⚡ Post-Install Commands

```bash
# Linux Lite has a built-in updater — use it, or run:
sudo apt update && sudo apt upgrade -y

# Install common tools
sudo apt install -y curl git wget htop neofetch

# If you code — install VS Code
sudo apt install -y code
```

---

## 🛠️ First Things to Do After Install

1. 🔄 Open **Lite Upgrade** from the desktop or menu → run all updates
2. 🖥️ Check **Welcome Screen** → it guides you through first steps
3. 🛡️ Install **Lite Tweaks** (pre-installed) → optimize for your hardware
4. 📦 Use **Software Center** to install apps without terminal

---

## ⚡ Speed Tips for Old Hardware

```bash
# Disable unnecessary startup services
sudo systemctl disable bluetooth.service   # if no Bluetooth
sudo systemctl disable cups.service        # if no printer

# Check what's using RAM
htop

# Reduce swappiness (write to disk less often)
echo 'vm.swappiness=10' | sudo tee -a /etc/sysctl.conf
sudo sysctl -p
```

---

## 💡 Tips

- **Lite Tweaks** (pre-installed) has a one-click option to reduce RAM usage — use it
- Keep the browser light: use **Firefox** with uBlock Origin, avoid Chrome on low RAM
- Linux Lite's **Help section** (in the menu) is genuinely good — check it before googling

---

## 🔗 Resources

- 📖 [Linux Lite Wiki](https://www.linuxliteos.com/wiki/)
- 💬 [Linux Lite Forums](https://www.linuxliteos.com/forums/)
- 📋 Related playbook: [`playbooks/01-old-laptop-revive.md`](../playbooks/01-old-laptop-revive.md)

---

*Part of [linux-for-every-machine](../README.md) · Copyright © 2026 Azhar Shakeel*
