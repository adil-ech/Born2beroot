# 🔐 Born2beroot

`Born2beroot` is a system administration project from the 42 curriculum focused on setting up a secure Linux-based virtual machine. It aims to introduce students to fundamental sysadmin practices, including user management, firewall configuration, and securing a Linux environment.

## 📚 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Installation](#-installation)
- [Configuration Summary](#-configuration-summary)
- [Security Practices](#-security-practices)
- [License](#-license)
- [Notes](#-notes)

## 📖 Overview

The objective of this project is to configure a virtual machine (Debian or Rocky Linux) with:

- Strong user and password policies
- SSH access control
- A working UFW firewall
- Sudo rights limited to specific users
- Hostname and partition setup

It tests your knowledge of basic Linux commands, system configuration, user permissions, and security policies.

## ✨ Features

- ✅ Virtual Machine setup with VirtualBox or UTM
- ✅ Custom hostname and partitioning with LVM
- ✅ Strong password policies via PAM
- ✅ Sudo rights via sudoers file and user groups
- ✅ SSH access on custom port (optional)
- ✅ UFW firewall enabled with strict rules
- ✅ Cron job monitoring unauthorized file edits

## ⚙️ Installation

You must create a virtual machine using Debian (preferred) or Rocky Linux. The installation includes:

1. Manual partitioning using LVM (with `/`, `swap`, and optionally `/home`)
2. Installation of required packages: `sudo`, `ufw`, `cron`, etc.
3. Configuration of hostname and `/etc/hosts`
4. Setup of password policy via `/etc/login.defs` and `PAM`
5. Adding user to the sudo group and restricting root access

## 🛠️ Configuration Summary

- `sudo` rights given only to users in the `sudo` group
- Password must meet complexity requirements (min length, uppercase, digits, special chars)
- UFW must be configured to allow only necessary ports
- SSH (optional): may require port change and disable root login
- Monitoring with `cron` to detect changes in `/etc/passwd`, `/etc/shadow`, etc.

## 🔒 Security Practices

- 🔐 Password policies enforced via `PAM`
- 🔐 Root login disabled in SSH (optional but recommended)
- 🔐 UFW (Uncomplicated Firewall) enabled with default deny policy
- 🔐 Access logs reviewed and maintained

## 📬 License

This project is part of the 42 Network curriculum and should be used for educational purposes only.

## 🗒️ Notes

I wrote down all my personal notes, research, and useful references while working on this project. You can view them here:
👉 [My Born2beroot Notes](https://www.tldraw.com/ro/8xZItjgP75YMRQuwHrJXb?d=v-7942.-6726.24636.12228.page)

## 📄 Subject PDF

You can read the official 42 Born2beroot subject here:  
👉 [Born2beroot Subject PDF](./en.subject.pdf)
