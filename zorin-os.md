# 🔵 Zorin OS — Distro Guide

> *The most visually polished Linux for Windows and macOS switchers. Looks premium, works reliably.*

---

## 📋 Quick Summary

| Property | Details |
|----------|---------|
| 🏷️ Based on | Ubuntu LTS |
| 🎯 Primary use | Daily desktop, Windows/macOS replacement |
| 💾 Minimum RAM | 2 GB (4 GB recommended) |
| 💿 Minimum storage | 15 GB |
| 👤 Target user | Beginners, design-conscious users |
| 🌐 Official site | [zorin.com/os](https://zorin.com/os/) |

---

## ✅ When to Use Zorin OS

- You want a **beautiful, polished desktop** right out of the box
- You are **switching from Windows or macOS** and want a familiar look
- You want **zero setup friction** — Zorin handles everything visually
- You want a **stable Ubuntu LTS base** without Ubuntu's interface choices

## ❌ When NOT to Use Zorin OS

- You need the **Pro edition features** but don't want to pay (Core is free, Pro is paid)
- You want a **server or minimal OS** — not Zorin's purpose
- You prefer **maximum performance** over visual polish on old hardware

---

## 💻 Hardware Requirements

| Spec | Minimum | Recommended |
|------|---------|-------------|
| 🖥️ CPU | 64-bit dual-core | 64-bit quad-core |
| 🧠 RAM | 2 GB | 4 GB+ |
| 💾 Storage | 15 GB | 40 GB+ |
| 🖥️ Display | 800×600 | 1920×1080 |

---

## 🎯 Which Edition to Choose

| Edition | Cost | Best For |
|---------|------|---------|
| 🆓 **Core** | Free | Most users — full-featured desktop |
| 💎 **Pro** | Paid | Extra layouts (macOS-style, Windows 11-style), extra apps |
| 💾 **Lite** | Free | Low-end hardware (2 GB RAM) |
| 🎓 **Education** | Free | Schools and students |

**Start with Core** — it's free and complete.

---

## 📥 Download

1. Go to **[zorin.com/os/download](https://zorin.com/os/download/)**
2. Select **Core** (free)
3. Download the **64-bit ISO**

---

## 🔧 Install

```bash
# Flash to USB on Linux
sudo dd if=ZorinOS-*.iso of=/dev/sdX bs=4M status=progress && sync
```

1. Boot from USB
2. Select **Try or Install Zorin OS**
3. Click **Install Zorin OS**
4. Choose language, keyboard, timezone
5. ✅ Check **"Install third-party software"**
6. Select **Erase disk and install** for a clean setup
7. Create user and password → Install → Reboot

---

## ⚡ Post-Install Commands

```bash
# Update system
sudo apt update && sudo apt upgrade -y

# Install essentials
sudo apt install -y curl git wget htop build-essential

# Install VS Code (same as Mint)
sudo apt install -y code
```

---

## 💡 Tips

- Zorin ships with a **Windows layout by default** — looks familiar immediately
- Go to **Zorin Appearance** settings to switch between Windows-style, macOS-style, and minimal layouts
- The **Software store** is simple and graphical — great for non-terminal users
- Zorin Core includes everything most users need: browser, office, media player

---

## 🔗 Resources

- 📖 [Zorin OS Help](https://help.zorin.com)
- 📋 Related playbook: [`playbooks/02-from-windows-to-linux-desktop.md`](../playbooks/02-from-windows-to-linux-desktop.md)

---

*Part of [linux-for-every-machine](../README.md) · Copyright © 2026 Azhar Shakeel*
