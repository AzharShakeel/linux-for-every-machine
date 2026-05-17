# Playbook: Move from Windows to Linux Desktop

## Goal
Set up a stable daily Linux desktop with minimal friction.

## Steps
1. Pick Linux Mint or Zorin OS.
2. Back up personal files from Windows.
3. Create installation USB and boot live environment.
4. Test Wi-Fi, sound, graphics, and keyboard.
5. Install Linux and apply all updates.
6. Install daily-use apps and browser sync.

## Post-install baseline
```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y git curl vlc gnome-software
```
