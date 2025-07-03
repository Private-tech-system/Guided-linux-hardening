![AI Assisted](https://img.shields.io/badge/AI%20Assisted-ChatGPT-blueviolet)

# 🔐 Secure Boot Enabled

## Overview

Secure Boot is a firmware-level security feature that ensures only trusted and signed bootloaders and kernels are executed during the system startup process. This prevents unauthorized code or malware from loading before the OS.

## ✅ Why Secure Boot Matters

- Blocks malicious bootloaders and unauthorized kernel modules
- Helps ensure system integrity at boot time
- Strengthens UEFI-based system security

## 🛠️ How It Was Enabled

Secure Boot was enabled via BIOS/UEFI firmware settings. The Linux Mint installation was verified to support Secure Boot with signed kernel modules.

## 🔎 Verifying Secure Boot Status

To check if Secure Boot is active:

```bash
mokutil --sb-state
```

Expected output:
```
SecureBoot enabled
```

You can also verify with:

```bash
dmesg | grep -i secure
```

## 🧠 Notes

- Secure Boot is especially important for mobile or travel scenarios.
- Combined with full disk encryption and UEFI settings, it creates a solid trust chain.

---

### 🧾 AI Transparency Note

> This documentation was created with the assistance of ChatGPT to ensure accuracy, consistency, and professional formatting. All actions were performed manually on the system.
