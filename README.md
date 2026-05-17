

<div align="center">

# 🐧 linux-for-every-machine

### The right Linux distribution for every machine, every goal, every user.
### No hype. No distro wars. Just clear choices and commands that work.

**Opinionated · Practical · Battle-tested**

---

[![Last Commit](https://img.shields.io/github/last-commit/AzharShakeel/linux-for-every-machine?style=flat-square&color=238636&labelColor=161b22)](https://github.com/AzharShakeel/linux-for-every-machine)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue?style=flat-square&color=0366d6&labelColor=161b22)](LICENSE)
[![Distros](https://img.shields.io/badge/Distros-10%2B-brightgreen?style=flat-square&color=1f6feb&labelColor=161b22)]()
[![Stars](https://img.shields.io/github/stars/AzharShakeel/linux-for-every-machine?style=flat-square&color=e3b341&labelColor=161b22)]()

</div>

---

## 💡 What This Is

> *Most Linux content says "use whatever you like." That is useless when you have a specific machine and a specific goal.*

This repository is a **practical, opinionated guide** to choosing the right Linux distribution — and actually setting it up — for four real-world scenarios:

- 🔐 Ethical hacking and security labs
- 🖥️ Normal daily desktop use
- 💾 Old and low-end computers
- 🌐 Home servers and VPS machines

No 50-distro confusion. No theoretical comparisons. Just **clear picks, step-by-step playbooks, and commands that matter** on real hardware.

---

## 📌 Table of Contents

- [👥 Who This Is For](#-who-this-is-for)
- [⚡ Quick Distro Matrix](#-quick-distro-matrix-2026)
- [📁 Repo Structure](#-repo-structure)
- [🗺️ How to Use This Repo](#️-how-to-use-this-repo)
- [📐 Scope and Philosophy](#-scope-and-philosophy)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

---

## 👥 Who This Is For

- 🎓 **Students and developers** who want a stable, fast daily driver
- 🔐 **Security learners** who want a Kali/Parrot lab without destroying their main OS
- 💻 **People with old laptops** who want to revive them instead of buying new hardware
- 🏠 **Home-lab and VPS users** who want a simple, secure server setup

You don't need to know everything about Linux.
You just need to know **which distro to pick** and **which commands to run**.

---

## ⚡ Quick Distro Matrix (2026)

| 🎯 I want… | ✅ Recommended Distros | 📝 Notes |
|------------|----------------------|----------|
| 🔐 Ethical hacking / security lab | **Kali Linux, Parrot OS** | Purpose-built for penetration testing, ships with large toolsets and strong documentation |
| 🖥️ Normal desktop (switching from Windows) | **Linux Mint, Zorin OS, Pop!_OS, Ubuntu LTS** | Beginner-friendly, stable, familiar interface, easy install |
| 💾 Old / low-end laptop (2–4 GB RAM) | **Linux Lite, MX Linux, Puppy Linux** | Lightweight, fast, proven on aging hardware |
| 🌐 Stable home server / VPS | **Debian, Ubuntu Server LTS, AlmaLinux, Rocky** | Long-term support, production-grade, strong community |

Each distro has its own detailed guide in [`distro-guides/`](./distro-guides/).

---

## 📁 Repo Structure

```
linux-for-every-machine/
│
├── 📋 README.md
├── 📄 LICENSE
│
├── 📦 distro-guides/          ← One file per distro
│   ├── kali-linux.md
│   ├── parrot-os.md
│   ├── linux-mint.md
│   ├── zorin-os.md
│   ├── linux-lite.md
│   ├── mx-linux.md
│   ├── debian-server.md
│   ├── ubuntu-server.md
│   ├── almalinux.md
│   └── rocky-linux.md
│
├── 🗺️ playbooks/              ← Scenario-based step-by-step flows
│   ├── 01-old-laptop-revive.md
│   ├── 02-from-windows-to-linux-desktop.md
│   ├── 03-ethical-hacking-lab.md
│   └── 04-home-server-or-vps.md
│
├── ⚡ cheatsheets/            ← Commands for quick copy-paste
│   ├── linux-basics.md
│   ├── package-managers.md
│   ├── networking-and-ssh.md
│   ├── server-essentials.md
│   └── hacking-lab-commands.md
│
└── 💬 opinions/               ← Personal notes and comparisons
    ├── why-i-chose-mx-linux-for-old-hardware.md
    └── advanced-distros-arch-fedora-nixos.md
```

| Folder | Purpose |
|--------|---------|
| 📦 `distro-guides/` | When to use it, hardware requirements, install steps, post-install commands |
| 🗺️ `playbooks/` | Full scenario walkthroughs from zero to working setup |
| ⚡ `cheatsheets/` | Pure commands — no explanation, just copy and run |
| 💬 `opinions/` | Personal views kept separate from neutral guides |

---

## 🗺️ How to Use This Repo

### Step 1 — Identify Your Scenario

Ask yourself one question:

- *"I want a hacking lab on my laptop."* → `playbooks/03-ethical-hacking-lab.md`
- *"I want to make my 4 GB RAM laptop usable."* → `playbooks/01-old-laptop-revive.md`
- *"I want to replace Windows as my main OS."* → `playbooks/02-from-windows-to-linux-desktop.md`
- *"I want to run a small home server or VPS."* → `playbooks/04-home-server-or-vps.md`

### Step 2 — Pick a Distro

Use the matrix above, then open the matching file in `distro-guides/`.

```
distro-guides/kali-linux.md
distro-guides/linux-lite.md
distro-guides/mx-linux.md
distro-guides/debian-server.md
```

### Step 3 — Follow the Playbook

Go to `playbooks/` and pick the scenario that matches your goal. Every playbook is a linear, step-by-step flow from fresh hardware to working system.

### Step 4 — Use the Cheatsheets

When you need a command fast:

```
cheatsheets/linux-basics.md
cheatsheets/package-managers.md
cheatsheets/networking-and-ssh.md
cheatsheets/server-essentials.md
cheatsheets/hacking-lab-commands.md
```

---

## 📐 Scope and Philosophy

**This repo is NOT:**

- ❌ A full Linux textbook
- ❌ A deep dive into every distro's internals
- ❌ A replacement for official documentation

**This repo IS:**

- ✅ A **decision guide** — which distro for which machine and goal
- ✅ A set of **simple playbooks** you can follow line by line
- ✅ A collection of **commands that actually matter** for real use

> *If you want to go deeper into a specific distro, always read the official documentation from that project's website. This repo gives you the starting point — not the whole map.*

---

## 🤝 Contributing

If you:

- Tested a distro on real hardware (old laptop, server, VM, etc.)
- Have a better playbook for a specific scenario
- Want to add commands or fix mistakes in cheatsheets

You can:

1. 🍴 Fork this repo
2. 🌿 Create a branch (`feature/improve-linux-lite-guide`)
3. ✏️ Commit your changes with clear messages
4. 📬 Open a pull request explaining:
   - What you changed
   - Which hardware you tested on (if relevant)
   - Any references (official docs, guides)

**Please keep the style:** practical, tested, no hype, no distro wars.

---

## ⭐ Support This Repository

If this helped you:

- ⭐ **Star this repo** so others can find it
- 🔀 **Fork it** and improve what you know best
- 📢 **Share it** with someone who's struggling to pick a distro

---

## 📄 License

This project is licensed under the **[MIT License](LICENSE)** — free to use, share, and build upon.

Copyright © 2026 **Azhar Shakeel**

---

<div align="center">

*Built for people who want Linux to work — not just exist on their machine.*

**[⬆ Back to Top](#-linux-for-every-machine)**

</div>
