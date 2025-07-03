![AI Assisted](https://img.shields.io/badge/AI%20Assisted-ChatGPT-blueviolet)

# 📝 System Auditing with auditd

## Overview

auditd is the user-space component to the Linux Auditing System. It provides detailed logs of system events such as file access, user actions, and privilege escalations.

## 🛠️ Installation

```bash
sudo apt update
sudo apt install auditd audispd-plugins
```

## 🧪 Basic Commands

- Check service status:

```bash
sudo systemctl status auditd
```

- View logs:

```bash
sudo ausearch -x sudo
sudo aureport -au
```

## 🔒 Why It Matters

- Detects suspicious activity
- Tracks user commands and privilege use
- Essential for compliance and forensic readiness

---

### 🧾 AI Transparency Note

> This documentation was created with the assistance of ChatGPT to ensure accuracy, consistency, and professional formatting. All actions were performed manually on the system.
