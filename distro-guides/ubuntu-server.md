# Ubuntu Server (LTS) – Guide

Ubuntu Server LTS is a strong default when you want broad compatibility, large community support, and a predictable long-term maintenance cycle. This guide gives a clean starting path for both home-lab and cloud deployments.

## When to use

- You want a stable Linux server with long-term support.
- You need broad package availability and large community docs.
- You are deploying home-lab services or cloud VPS workloads.

## Minimum hardware & target users

- 2 GB RAM minimum (4 GB recommended).
- 64-bit CPU.
- Best for beginners to intermediate server users.

## Download

- Official site: https://ubuntu.com/download/server
- Download the latest **LTS** image.

## Install

1. Create a bootable USB from the ISO.
2. Boot from USB and start the installer.
3. Configure storage, network, user, and SSH options.
4. Reboot into the installed system.

## Post-install commands

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y ufw fail2ban
sudo ufw allow OpenSSH
sudo ufw enable
```
