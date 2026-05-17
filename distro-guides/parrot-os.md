# 🦜 Parrot OS — Distro Guide

> *A lighter, privacy-focused alternative to Kali. Great for hacking labs and secure daily use on the same machine.*

---

## 📋 Quick Summary

| Property | Details |
|----------|---------|
| 🏷️ Based on | Debian (testing) |
| 🎯 Primary use | Ethical hacking, privacy, daily desktop |
| 💾 Minimum RAM | 1 GB (2 GB recommended) |
| 💿 Minimum storage | 16 GB |
| 👤 Target user | Beginner-friendly to intermediate |
| 🌐 Official site | [parrotsec.org](https://parrotsec.org) |

---

## ✅ When to Use Parrot OS

- You want a **hacking distro that is also usable as a daily desktop**
- You have a **machine with limited RAM** (lighter than Kali)
- You care about **privacy and anonymity** alongside security tools
- You are a **beginner to ethical hacking** — Parrot's Home edition is gentler
- You want a clean, polished MATE desktop with security tools built in

## ❌ When NOT to Use Parrot OS

- You need the **absolute latest version of every Kali tool** — Kali has a larger and more frequently updated toolset
- You want the **industry-standard hacking distro** for certifications (most courses assume Kali)

---

## 💻 Hardware Requirements

| Spec | Minimum | Recommended |
|------|---------|-------------|
| 🖥️ CPU | 64-bit dual-core | 64-bit quad-core |
| 🧠 RAM | 1 GB | 2 GB+ |
| 💾 Storage | 16 GB | 40 GB+ |
| 🌐 Network | Required | Required |

> 💡 Parrot is noticeably lighter than Kali — a real advantage on older machines.

---

## 🎯 Which Edition to Choose

| Edition | Who It's For |
|---------|-------------|
| 🔐 **Security** | Ethical hacking and penetration testing |
| 🏠 **Home** | Privacy-focused daily desktop — no hacking tools |
| ☁️ **Cloud** | Server/VPS deployment |

Start with **Security** if you want hacking tools. Start with **Home** if you want a private daily OS.

---

## 📥 Download

1. Go to **[parrotsec.org/download](https://parrotsec.org/download/)**
2. Select your edition (Security or Home)
3. Download the **64-bit ISO**
4. Verify the checksum before flashing

---

## 🔧 Install

```bash
# Flash to USB on Linux
sudo dd if=Parrot-security-*.iso of=/dev/sdX bs=4M status=progress && sync
```

1. Boot from USB
2. Select **Install** or **Graphical Install**
3. Choose language, timezone, keyboard
4. Partition: **Guided — use entire disk** for a clean setup
5. Create user and password
6. Reboot

---

## ⚡ Post-Install Commands

```bash
# Full system update
sudo apt update && sudo apt full-upgrade -y

# Install useful essentials
sudo apt install -y curl git wget htop neofetch

# Update Parrot's tool collection
sudo parrot-upgrade
```

---

## 💡 Tips

- Use **Parrot Home** if you want privacy tools (Tor, Firejail) without the hacking suite
- Parrot ships with **AnonSurf** — routes traffic through Tor with one command:
  ```bash
  sudo anonsurf start
  ```
- Both Kali and Parrot are valid — pick Kali for courses/certs, Parrot for lightweight daily+hacking combo

---

## 🔗 Resources

- 📖 [Parrot Official Docs](https://parrotsec.org/docs/)
- 📋 Related playbook: [`playbooks/03-ethical-hacking-lab.md`](../playbooks/03-ethical-hacking-lab.md)

---

*Part of [linux-for-every-machine](../README.md) · Copyright © 2026 Azhar Shakeel*
