![AI Assisted](https://img.shields.io/badge/AI%20Assisted-ChatGPT-blueviolet)

# 🔐 Full Disk Encryption via LUKS

## Overview

Full disk encryption (FDE) was configured on my system using LUKS (Linux Unified Key Setup). This ensures that all data at rest is encrypted and inaccessible without the proper passphrase, even if the disk is physically stolen.

## 🔎 Why It Matters

- Protects sensitive files and credentials at rest
- Helps ensure confidentiality in case of physical theft or loss
- Prevents offline tampering or cloning of the OS disk
- Strong defense layer during travel or remote work

## 🔧 How It Was Configured

This system was encrypted during installation using the default LUKS full disk encryption option provided by the Linux Mint installer. All partitions except `/boot` were encrypted.

### 💡 Key Configuration Points:
- 🔐 Encrypted root and home partitions
- ⌨️ Passphrase prompt at boot before OS loads
- 🛡️ Integrated with GRUB for early boot decryption
- 🔁 Swap partition also encrypted

## 🧪 Testing Encryption

You can verify LUKS encryption is active with:

```bash
lsblk -f
```

Look for `crypto_LUKS` listed under TYPE and `luks-<UUID>` under NAME or MOUNTPOINT.

To check details about the encrypted volume:

```bash
sudo cryptsetup status <name>
```

Replace `<name>` with the LUKS mapping (e.g., `sda3_crypt` or `luks-xxxx`).

## 🧠 Notes

- LUKS provides strong AES-256 encryption by default.
- The encryption key is protected by a passphrase.
- It’s important to back up recovery keys or use a secure keyfile strategy for recovery.

---

### 🧾 AI Transparency Note

> This documentation was created with the assistance of ChatGPT to ensure accuracy, consistency, and professional formatting. All actions were performed manually on the system.
