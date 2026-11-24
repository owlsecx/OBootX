# 🦉 OBootX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OCore-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OBootX** — Linux Boot-Chain Security Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OBootX is an offline, read-only auditor for the Linux boot chain, covering GRUB2, systemd-boot, the kernel command line, Secure Boot/MOK, initramfs and /boot & ESP layout. It flags weak or missing bootloader passwords, dangerous kernel parameters, Secure Boot gaps and secrets embedded in initramfs images, with all secrets masked. It can audit the live host or a mounted image via --root, mapping findings to a score, A+…F grade and hardened templates.

---

## ✨ Features

- GRUB2 checks: superusers, pbkdf2 passwords, unrestricted/recovery entries, cryptodisk
- systemd-boot checks: editor, timeout, auto-firmware and per-entry kernel options
- Kernel cmdline analysis: init=/bin/sh, rd.break, KASLR, mitigations, lockdown
- Secure Boot / MOK review and stdlib cpio initramfs scanning (gz/xz)
- /boot, ESP and grub.cfg permissions with all secrets masked
- Export TXT/MD/JSON/CSV/SARIF, --demo self-test and CI fail-on gates

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OBootX --scan
./OBootX --root /mnt/image --scan --format json -o report.json --fail-on high
./OBootX --demo
./OBootX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OBootX --help   # watch every network call
firejail --net=none ./OBootX --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
