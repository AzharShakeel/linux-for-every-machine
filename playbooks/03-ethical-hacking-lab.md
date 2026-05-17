# Playbook: Build an Ethical Hacking Lab

This guide emphasizes legal, isolated, and repeatable lab setup so you can learn security safely. It helps you avoid common beginner mistakes like mixing offensive tools with your primary daily environment.

## Goal
Create a safe, isolated security-learning environment.

## Steps
1. Use Kali Linux or Parrot OS in a VM first.
2. Keep your normal daily OS separate.
3. Create internal lab network in VirtualBox/VMware.
4. Add test targets (Metasploitable, DVWA, etc.).
5. Update tools and document your lab setup.

## Post-install baseline
```bash
sudo apt update && sudo apt full-upgrade -y
sudo apt install -y kali-linux-top10
```
