> 🛡️ **Disclaimer: AI-Guided, Manually Verified Hardening**
>
> This Linux Mint Hardening repository documents the security configuration of my personal system. All steps, installations, and configurations were **performed manually** by me in a live lab environment.
>
> I used ChatGPT (AI) as a **guidance and documentation tool** to:
> - Help structure my notes
> - Explain steps clearly
> - Generate `.md` files and write-ups based on what I tested
>
> Every command, setting, and configuration in this repo has been **manually executed and verified** by me on my own machine. This project reflects my personal effort to build and maintain a secure Linux Mint system while documenting the learning process professionally.

![AI-Assisted, Lab Verified](https://img.shields.io/badge/AI--Assisted-Lab--Verified-blue?style=for-the-badge&logo=linux)


# Guided Linux Hardening (Linux Mint)

This repository documents the step-by-step hardening of a personal Linux Mint system, guided entirely through ChatGPT.

## 🔐 Purpose

The goal of this project is to improve system security by following a structured hardening process, while building a deeper understanding of why each step is taken.

This is not a one-click solution or automated script — every change was made manually, with care and learning involved along the way.

## 🤖 AI Guidance

This hardening process was guided interactively by ChatGPT, acting as a security assistant. Commands were run manually, and understanding was prioritized over automation.

## 🛡️ Security Features Applied

- ✅ SSH hardening (custom port, key-only auth, no root login)
- ✅ Full disk encryption (LUKS)
- ✅ AppArmor enforcement
- ✅ AIDE (file integrity checking)
- ✅ `auditd` (audit logs for system activity)
- ✅ `rkhunter` and `chkrootkit` (rootkit detection)
- ✅ `ufw` firewall enabled
- ✅ ClamAV antivirus
- ✅ Kernel lockdown mode enabled
- ✅ Secure Boot (BIOS level)
- ✅ Minimal services and package cleanup
- ✅ Webcam + Bluetooth disabled (BIOS)
- ✅ Log rotation and alerting for tamper detection

## 📚 Educational Value

This is not a professional hardening benchmark. It's a learning-driven journey to better understand Linux security — and to serve as a reference for others beginning their own hardening process.

## 🧠 Credits

Every security step was completed manually after being guided by ChatGPT (GPT-4o). This is not a solo or expert-based project — it's a documented walk-through with AI as a teacher.

---

*Use this for inspiration, not for blind copying. Understand your system before applying security changes.*


