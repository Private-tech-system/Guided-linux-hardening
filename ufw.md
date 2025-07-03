![AI Assisted](https://img.shields.io/badge/AI%20Assisted-ChatGPT-blueviolet)

# 🔥 UFW Firewall Configuration

## Overview

UFW (Uncomplicated Firewall) is a simple front-end for iptables that makes managing a firewall on Linux easier.

## 🛠️ Installation & Enablement

```bash
sudo apt update
sudo apt install ufw
sudo ufw enable
```

## 🔒 Basic Usage

- Allow SSH on custom port:

```bash
sudo ufw allow 58222/tcp
```

- Deny all incoming traffic by default:

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

- Check status:

```bash
sudo ufw status verbose
```

---

### 🧾 AI Transparency Note

> This documentation was created with the assistance of ChatGPT to ensure accuracy, consistency, and professional formatting. All actions were performed manually on the system.
