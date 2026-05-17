# Playbook: Revive an Old Laptop (2–4 GB RAM)

## Goal
Make an old machine fast and usable again with a lightweight Linux distro.

## Steps
1. Choose Linux Lite (beginner-friendly) or MX Linux (faster, slightly advanced).
2. Back up all important data.
3. Download ISO from official website and create bootable USB.
4. Boot from USB and test live session.
5. Install using full-disk install if this is a clean setup.
6. Update system and remove unneeded startup apps.

## Post-install baseline
```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y firefox vlc htop git
```
