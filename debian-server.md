# 🌀 Debian Server — Distro Guide

> *The most stable Linux foundation that exists. If you want a server that runs for years without touching it, Debian is the answer.*

---

## 📋 Quick Summary

| Property | Details |
|----------|---------|
| 🏷️ Based on | Independent (the base of Ubuntu, Mint, MX, and hundreds more) |
| 🎯 Primary use | Home servers, VPS, production servers |
| 💾 Minimum RAM | 512 MB (1 GB+ recommended for server workloads) |
| 💿 Minimum storage | 10 GB |
| 👤 Target user | Intermediate to advanced — comfortable with CLI |
| 🌐 Official site | [debian.org](https://www.debian.org) |

---

## ✅ When to Use Debian Server

- You want a **long-term stable server** — Debian Stable releases are updated every 2-3 years
- You want to **self-host** (Nextcloud, Nginx, PostgreSQL, etc.)
- You want a **VPS base OS** that is predictable and well-documented
- You want the **maximum control** with **minimum bloat** — Debian server is pure CLI
- You want something that will **not break from updates** — Debian's stable branch is extremely conservative

## ❌ When NOT to Use Debian

- You need **very recent software** — Debian Stable ships older (but battle-tested) package versions
- You are a **complete beginner to servers** — start with Ubuntu Server (more guides, snaps, Canonical support)

---

## 💻 Hardware Requirements

| Spec | Minimum | Recommended |
|------|---------|-------------|
| 🖥️ CPU | 64-bit (any modern CPU) | 64-bit dual-core+ |
| 🧠 RAM | 512 MB | 1–2 GB+ for server apps |
| 💾 Storage | 10 GB | 20 GB+ |
| 🌐 Network | Required | Wired preferred for servers |

---

## 📥 Download

1. Go to **[debian.org/distrib](https://www.debian.org/distrib/)**
2. Download **"Small CD/USB"** — the netinstall ISO (~400 MB)
3. This downloads packages during install — requires internet connection

> 💡 For servers, netinstall is preferred — you get only what you install.

---

## 🔧 Install (Server/Minimal)

```bash
# Flash netinstall ISO
sudo dd if=debian-*-netinst.iso of=/dev/sdX bs=4M status=progress && sync
```

1. Boot from USB
2. Select **Install** (not graphical) — faster for servers
3. Choose language, location, keyboard
4. Configure network and hostname (e.g., `debian-server`)
5. Create root password AND a regular user
6. Partition: **Guided — use entire disk** → all files in one partition
7. On software selection screen:
   - ✅ **SSH server** — essential
   - ✅ **Standard system utilities**
   - ❌ Uncheck everything else for a minimal server
8. Install GRUB → reboot

---

## ⚡ Post-Install Commands

```bash
# Login as your user, then switch to root
su -

# Or add your user to sudo first
apt install -y sudo
usermod -aG sudo yourusername
# Log out and back in

# Full system update
sudo apt update && sudo apt upgrade -y

# Install essential tools
sudo apt install -y curl wget git htop ufw fail2ban unzip

# Enable firewall
sudo ufw allow OpenSSH
sudo ufw enable

# Check firewall status
sudo ufw status
```

---

## 🛡️ Basic Security Setup

```bash
# Enable automatic security updates
sudo apt install -y unattended-upgrades
sudo dpkg-reconfigure --priority=low unattended-upgrades

# Harden SSH — edit config
sudo nano /etc/ssh/sshd_config
# Set: PasswordAuthentication no   (after adding SSH keys)
# Set: PermitRootLogin no
sudo systemctl restart sshd

# Check who is logged in
who
last

# Check listening ports
sudo ss -tulnp
```

---

## 🌐 Common Server Installs

```bash
# Nginx web server
sudo apt install -y nginx
sudo systemctl enable nginx && sudo systemctl start nginx

# PostgreSQL database
sudo apt install -y postgresql
sudo systemctl enable postgresql

# MariaDB (MySQL-compatible)
sudo apt install -y mariadb-server
sudo mysql_secure_installation

# Docker
curl -fsSL https://get.docker.com | sh
sudo usermod -aG docker $USER
```

---

## 💡 Tips

- Always set up **SSH key authentication** before disabling password auth
- Use **UFW** (pre-installed on Ubuntu, needs install on Debian) — simple firewall rules
- Take a **snapshot before major changes** if on a VPS
- Debian Stable = old but unbreakable; Debian Testing = newer but less tested

---

## 🔗 Resources

- 📖 [Debian Admin Handbook](https://www.debian.org/doc/manuals/debian-handbook/)
- 📋 Related playbook: [`playbooks/04-home-server-or-vps.md`](../playbooks/04-home-server-or-vps.md)

---

*Part of [linux-for-every-machine](../README.md) · Copyright © 2026 Azhar Shakeel*
