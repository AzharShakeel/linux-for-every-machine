# Rocky Linux – Guide

Rocky Linux targets users who need long-term consistency, RHEL ecosystem compatibility, and production-grade stability. This guide helps you deploy a reliable server foundation with minimal guesswork.

## When to use

- You need a reliable RHEL-compatible server distribution.
- You prefer predictable lifecycle and stable updates.

## Minimum hardware & target users

- 2 GB RAM minimum (4 GB recommended).
- 64-bit CPU.
- Best for admins and server-focused users.

## Download

- Official site: https://rockylinux.org
- Download the latest stable ISO.

## Install

1. Create bootable media with the ISO.
2. Run installer and set disk/network/user options.
3. Finish install and reboot.

## Post-install commands

```bash
sudo dnf update -y
sudo dnf install -y epel-release
sudo dnf install -y firewalld
sudo systemctl enable --now firewalld
```
