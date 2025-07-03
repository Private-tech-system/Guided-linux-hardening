![AI Assisted](https://img.shields.io/badge/AI%20Assisted-ChatGPT-blueviolet)

# 🛡️ Lynis Security Auditing

## Overview

Lynis is a powerful security auditing tool for Unix-based systems. It performs in-depth scans of the operating system, file permissions, security configurations, and installed software to identify potential vulnerabilities and improvement areas.

## 🔍 Why Use Lynis?

- Evaluates system hardening effectiveness
- Identifies insecure configurations
- Recommends improvements based on best practices
- Useful for both initial setup and ongoing security reviews

## 🛠️ Installation

Lynis was installed using:

```bash
sudo apt update
sudo apt install lynis
```

## 🧪 Running a Basic Audit

To perform a full system audit:

```bash
sudo lynis audit system
```

The tool provides a comprehensive report at the end with a security score and recommendations for hardening.

## 📄 Report Location

Results and logs are typically stored in:

```
/var/log/lynis.log
/var/log/lynis-report.dat
```

## 🧠 Notes

- A higher security score indicates a more hardened system.
- Always follow up on "suggestions" from the Lynis output.
- This tool is safe to run on production systems.

---

### 🧾 AI Transparency Note

> This documentation was created with the assistance of ChatGPT to ensure accuracy, consistency, and professional formatting. All actions were performed manually on the system.
