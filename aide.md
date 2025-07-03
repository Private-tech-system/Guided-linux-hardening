![AI Assisted](https://img.shields.io/badge/AI%20Assisted-ChatGPT-blueviolet)

# 🧾 File Integrity Monitoring with AIDE

## Overview

AIDE (Advanced Intrusion Detection Environment) is a file integrity checker that creates a baseline snapshot of your filesystem and alerts on any changes.

## 🛠️ Installation

```bash
sudo apt update
sudo apt install aide
```

## 🛠️ Initialization

```bash
sudo aideinit
sudo cp /var/lib/aide/aide.db.new /var/lib/aide/aide.db
```

## 🧪 Running Checks

```bash
sudo aide --check
```

Compare changes to detect tampering or unauthorized modifications.

---

### 🧾 AI Transparency Note

> This documentation was created with the assistance of ChatGPT to ensure accuracy, consistency, and professional formatting. All actions were performed manually on the system.
