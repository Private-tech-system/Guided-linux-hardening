![AI Assisted](https://img.shields.io/badge/AI%20Assisted-ChatGPT-blueviolet)

# 🕵️ Rootkit Detection with RKHunter

## Overview

RKHunter (Rootkit Hunter) is a Unix-based tool that scans for rootkits, backdoors, and local exploits by checking for known signatures and system anomalies.

## 🛠️ Installation

```bash
sudo apt update
sudo apt install rkhunter
```

## 🧪 Usage

To run a scan:

```bash
sudo rkhunter --update
sudo rkhunter --check
```

Use the `--sk` option to skip prompts:

```bash
sudo rkhunter --check --sk
```

## 📋 Notes

- Keep RKHunter updated regularly for latest rootkit definitions.
- Alerts may require manual review in `/var/log/rkhunter.log`.

---

### 🧾 AI Transparency Note

> This documentation was created with the assistance of ChatGPT to ensure accuracy, consistency, and professional formatting. All actions were performed manually on the system.
