# Playbook: Home Server or VPS Setup

## Goal
Deploy a small, secure Linux server for personal services.

## Steps
1. Pick Debian, Ubuntu Server LTS, AlmaLinux, or Rocky Linux.
2. Install minimal system with SSH enabled.
3. Create non-root sudo user and disable password SSH login.
4. Configure firewall and automatic updates.
5. Install only required services (Docker, Nginx, etc.).

## Security baseline
```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y ufw fail2ban
sudo ufw allow OpenSSH
sudo ufw enable
```
