# 🔴 Kali Linux — Distro Guide

> *The industry standard for penetration testing and ethical hacking. Powerful by design, dangerous if misused.*

---

## 📋 Quick Summary

| Property | Details |
|----------|---------|
| 🏷️ Based on | Debian (rolling) |
| 🎯 Primary use | Ethical hacking, penetration testing, CTFs |
| 💾 Minimum RAM | 2 GB (4 GB recommended) |
| 💿 Minimum storage | 20 GB |
| 👤 Target user | Intermediate — knows basic Linux and networking |
| 🌐 Official site | [kali.org](https://www.kali.org) |

---

## ✅ When to Use Kali

- You want a **dedicated ethical hacking / penetration testing** environment
- You are preparing for certifications like **OSCP, CEH, eJPT**
- You are doing **CTF competitions** or security research
- You want a distro that ships with **600+ security tools** pre-installed
- You are comfortable with the terminal and basic Linux concepts

## ❌ When NOT to Use Kali

- You are a **complete beginner** to Linux — start with Linux Mint or Ubuntu instead
- You want a **daily desktop** for browsing, coding, and office work — Kali is not designed for this
- You have **less than 4 GB RAM** and want a smooth experience

---

## 💻 Hardware Requirements

| Spec | Minimum | Recommended |
|------|---------|-------------|
| 🖥️ CPU | 64-bit dual-core | 64-bit quad-core |
| 🧠 RAM | 2 GB | 4 GB+ |
| 💾 Storage | 20 GB | 50 GB+ |
| 🌐 Network | Required | Required |

---

## 📥 Download

1. Go to **[kali.org/get-kali](https://www.kali.org/get-kali/)**
2. Select **Installer Images → 64-bit**
3. Download the **Installer** (not live) for a permanent install
4. Verify the SHA256 checksum before flashing

> ⚠️ **Always download from the official website only.** Third-party mirrors may serve modified ISOs.

---

## 🔧 Install

### Flash the ISO to USB

```bash
# On Linux — replace /dev/sdX with your USB device
sudo dd if=kali-linux-*.iso of=/dev/sdX bs=4M status=progress && sync

# Or use balenaEtcher (GUI) on any OS
```

### Installation Steps

1. Insert USB → boot from it (F12 / F2 / ESC at startup)
2. Select **Graphical Install**
3. Choose language, location, keyboard
4. Set hostname (e.g., `kali`)
5. Create user and strong password
6. Partition: **Guided — use entire disk** for clean install
7. Finish and reboot

---

## ⚡ Post-Install Commands

Run these immediately after first login:

```bash
# Update the system fully
sudo apt update && sudo apt full-upgrade -y

# Install the top 10 most-used hacking tools
sudo apt install -y kali-linux-top10

# Optional: install the full default toolset (large download)
sudo apt install -y kali-linux-default

# Install useful extras
sudo apt install -y curl git wget htop neofetch
```

---

## 🛠️ Essential Tools (Pre-installed)

| Category | Tools |
|----------|-------|
| 🔍 Reconnaissance | nmap, recon-ng, maltego |
| 🌐 Web Testing | Burp Suite, nikto, sqlmap, dirb |
| 📶 Wireless | aircrack-ng, wifite, kismet |
| 🔐 Password | john, hashcat, hydra |
| 🧪 Exploitation | Metasploit Framework |
| 📦 Forensics | autopsy, binwalk, volatility |

---

## 💡 Tips

- Run Kali in a **VM first** (VirtualBox or VMware) before bare-metal install
- Use **Kali in VM** for hacking labs, keep your main OS for daily use
- Never use Kali tools on networks or systems you do not own or have explicit permission to test
- Join [forums.kali.org](https://forums.kali.org) for community support

---

## 🔗 Resources

- 📖 [Kali Official Docs](https://www.kali.org/docs/)
- 📺 [TryHackMe](https://tryhackme.com) — beginner-friendly hacking labs
- 📺 [HackTheBox](https://www.hackthebox.com) — intermediate/advanced labs
- 📋 Related playbook: [`playbooks/03-ethical-hacking-lab.md`](../playbooks/03-ethical-hacking-lab.md)

---

*Part of [linux-for-every-machine](../README.md) · Copyright © 2026 Azhar Shakeel*
