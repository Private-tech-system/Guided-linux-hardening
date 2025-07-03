![AI Assisted](https://img.shields.io/badge/AI%20Assisted-ChatGPT-blueviolet)

# 🦠 Antivirus Protection with ClamAV

## Overview

ClamAV is an open-source antivirus engine designed to detect trojans, viruses, malware, and other malicious threats on Linux systems.

## 🛠️ Installation

```bash
sudo apt update
sudo apt install clamav clamav-daemon
```

Update virus definitions:

```bash
sudo freshclam
```

## 🧪 Usage

To scan a directory:

```bash
sudo clamscan -r /path/to/scan
```

For a full system scan:

```bash
sudo clamscan -r --bell -i /
```

## 🔁 Notes

- Regularly update with `freshclam`
- Consider running `clamd` for on-access scanning (resource-intensive)

---

### 🧾 AI Transparency Note

> This documentation was created with the assistance of ChatGPT to ensure accuracy, consistency, and professional formatting. All actions were performed manually on the system.
