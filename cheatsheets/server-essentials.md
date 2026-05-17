# Server Essentials Cheatsheet

Core admin commands used in early server setup and ongoing operations. These are the high-value checks you repeatedly use in production and home-lab workflows.

```bash
sudo useradd -m devuser
sudo usermod -aG sudo devuser
sudo systemctl status ssh
sudo journalctl -xe
sudo ufw status
sudo systemctl enable --now fail2ban
```
