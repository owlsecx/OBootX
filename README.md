# 🦉 OBootX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OCore-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OBootX** — Linux Boot-Chain Security Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Offline boot-chain security auditor — GRUB2, systemd-boot, kernel cmdline, Secure Boot, initramfs

---

## ✨ Features

- GRUB2 — superusers / password_pbkdf2, plaintext passwords (masked), --unrestricted entries, recovery entries, os-prober, cryptodisk, iterations
- systemd-boot — editor, timeout, auto-firmware, EFI shell entries, per-entry kernel options
- Kernel cmdline — init=/bin/sh, rd.break, single, debug-shell, KASLR, CPU mitigations, lockdown, module.sig_enforce, IOMMU, allocator hardening, audit=1, AppArmor / SELinux switches
- Secure Boot / MOK — mokutil text exports, efivars, setup mode, MOK validation, test / expired keys
- initramfs — initramfs-tools, dracut, dropbear, cryptsetup keyfiles, stdlib cpio (gz/xz) scanner
- /boot, ESP and grub.cfg permissions; LUKS layout
- Secrets masked everywhere; --root offline images
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Self-test --demo, CI gates --fail-on / --min-severity

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OBootX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
