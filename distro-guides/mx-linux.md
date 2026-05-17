# ⚙️ MX Linux — Distro Guide

> *The most popular independent Linux distro. Lightweight, fast, powerful, and runs beautifully on old hardware.*

---

## 📋 Quick Summary

| Property | Details |
|----------|---------|
| 🏷️ Based on | Debian Stable |
| 🎯 Primary use | Old hardware, daily desktop, power users |
| 💾 Minimum RAM | 1 GB (2 GB recommended) |
| 💿 Minimum storage | 15 GB |
| 👤 Target user | Intermediate — comfortable with Linux basics |
| 🌐 Official site | [mxlinux.org](https://mxlinux.org) |

---

## ✅ When to Use MX Linux

- You have an **old laptop (2–4 GB RAM)** and want maximum performance
- You want a **stable Debian base** without Debian's complex setup
- You want **more control** than Linux Lite but still want a polished desktop
- You want a distro that **consistently ranks #1 on DistroWatch** — battle-tested by millions
- You want systemd-free option (MX uses SysV init with optional systemd)

## ❌ When NOT to Use MX Linux

- You are a **complete beginner** — start with Linux Lite or Linux Mint
- You want **Ubuntu-based software** — MX is Debian-based (most things still work, but not identical)

---

## 💻 Hardware Requirements

| Spec | Minimum | Recommended |
|------|---------|-------------|
| 🖥️ CPU | 64-bit (32-bit available) | 64-bit dual-core |
| 🧠 RAM | 1 GB | 2 GB+ |
| 💾 Storage | 15 GB | 30 GB+ |
| 🖥️ Display | 1024×768 | 1366×768+ |

---

## 🎨 Which Edition

| Edition | Desktop | RAM Usage | Best For |
|---------|---------|-----------|---------|
| 🌟 **XFCE** | Lightweight, fast | ~350 MB | Old hardware — default recommendation |
| 🌀 **KDE** | Feature-rich, modern | ~600 MB | Newer hardware wanting full features |
| 🏠 **Fluxbox** | Minimal, ultra-light | ~200 MB | Very old hardware (1 GB RAM) |

**Pick XFCE** for old laptops. It's fast, stable, and highly customizable.

---

## 📥 Download

1. Go to **[mxlinux.org/MX-Download](https://mxlinux.org/MX-Download/)**
2. Select **MX-23 XFCE 64-bit** (recommended for most)
3. Download the ISO and verify SHA256

---

## 🔧 Install

```bash
# Flash to USB on Linux
sudo dd if=MX-*.iso of=/dev/sdX bs=4M status=progress && sync
```

1. Boot from USB
2. Click **Install MX Linux** on the desktop
3. Choose language, keyboard, timezone
4. Partition: **Use entire disk** for clean install
5. Create user and password
6. Reboot

---

## ⚡ Post-Install Commands

```bash
# Update system
sudo apt update && sudo apt upgrade -y

# Install essentials
sudo apt install -y curl git wget htop neofetch build-essential

# MX Package Installer also available in menu — use it for GUI installs
```

---

## 🛠️ MX-Specific Tools (Pre-installed)

| Tool | What It Does |
|------|-------------|
| 📦 **MX Package Installer** | GUI for finding and installing packages |
| ⚙️ **MX Tweak** | Fine-grained XFCE customization |
| 💾 **MX Snapshot** | Full system backup — use it before major changes |
| 🔄 **MX Updater** | Safe, controlled system updates |
| 🌐 **MX Network Assistant** | WiFi and network configuration |

---

## ⚡ Performance Tuning for Old Hardware

```bash
# Reduce swappiness
echo 'vm.swappiness=10' | sudo tee -a /etc/sysctl.conf
sudo sysctl -p

# Disable unused services
sudo systemctl disable bluetooth.service
sudo systemctl disable cups.service

# Check RAM usage
free -h

# See what processes eat RAM
htop
```

---

## 💡 Why MX Linux on Old Hardware

MX Linux uses **XFCE** — a desktop environment that is fast, stable, and fully-featured without being heavy. It uses **Debian Stable** underneath — meaning rock-solid packages with no unexpected breakage. The MX tools (Snapshot, Tweak, Package Installer) are genuinely better than most distro-specific tools. This is why it sits in the personal setup — see [`opinions/why-i-chose-mx-linux-for-old-hardware.md`](../opinions/why-i-chose-mx-linux-for-old-hardware.md).

---

## 🔗 Resources

- 📖 [MX Linux Wiki](https://mxlinux.org/wiki/)
- 💬 [MX Linux Forum](https://forum.mxlinux.org/)
- 📋 Related playbook: [`playbooks/01-old-laptop-revive.md`](../playbooks/01-old-laptop-revive.md)

---

*Part of [linux-for-every-machine](../README.md) · Copyright © 2026 Azhar Shakeel*
