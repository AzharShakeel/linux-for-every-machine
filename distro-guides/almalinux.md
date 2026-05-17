# AlmaLinux – Guide

AlmaLinux is ideal when you want enterprise-style behavior with RHEL compatibility and stable release expectations. This guide provides a practical baseline for dependable server deployments.

## When to use

- You want an enterprise-style, RHEL-compatible server OS.
- You need stability for production or long-running services.

## Minimum hardware & target users

- 2 GB RAM minimum (4 GB recommended).
- 64-bit CPU.
- Best for intermediate users and admins.

## Download

- Official site: https://almalinux.org
- Download the latest stable ISO.

## Install

1. Flash ISO to USB and boot installer.
2. Configure storage, timezone, network, and user.
3. Complete installation and reboot.

## Post-install commands

```bash
sudo dnf update -y
sudo dnf install -y epel-release
sudo dnf install -y firewalld fail2ban
sudo systemctl enable --now firewalld
```
