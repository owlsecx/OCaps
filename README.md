# 🦉 OCaps

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-Security-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0-cyan?style=flat-square"/>
</p>

> **OCaps** — part of the OwlSec Toolkit.

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OCaps shows exactly which Linux capabilities a process or binary holds and how risky they are. It decodes capability masks, reads the Cap* sets of any process and the security.capability xattr of files, and scans the filesystem for privileged binaries. It can also recommend the smallest capability set a workload needs and print the matching setcap, systemd and Docker settings.

---

## ✨ Features

- Decodes a hex capability mask into named capabilities with per-capability risk
- Process audit of /proc/PID/status sets (effective, permitted, inheritable, bounding, ambient)
- Reads file capabilities from the security.capability xattr (VFS cap v1/v2/v3)
- Filesystem scan for file-capability and setuid/setgid binaries, ranked by risk
- Recommends a minimal set and generates setcap / systemd / Docker --cap-drop commands
- Encyclopedia of 41 capabilities with ATT&CK and CWE references; set comparison; TXT/JSON/MD/CSV/SARIF reports

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OCaps                                      # interactive menu
./OCaps --decode 0000003fffffffff
./OCaps --pid 1234
./OCaps --scan /usr/bin
./OCaps --recommend web
```

Run `./OCaps --help` for the full list of options.

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
