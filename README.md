# 🦉 OXrdpX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-ONetwork-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OXrdpX** — Remote-Desktop Server Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview


OXrdpX is an offline, read-only xrdp and RDP server configuration auditor that parses xrdp.ini, sesman.ini and related files with stdlib-only parsers. It evaluates transport encryption (TLS vs legacy RDP security), certificate and key settings, authentication and session policy, and exposed listener addresses. Secrets are masked, findings are mapped to CWE and MITRE ATT&CK, and reports export to TXT, Markdown, JSON, CSV or SARIF.

---

## ✨ Features


- Parsers for xrdp.ini and sesman.ini (security layer, crypt level, listener, session directives)
- Transport checks: security_layer/negotiate vs rdp, tls_ciphers, min TLS version and legacy RDP security
- Certificate and key review (certificate/key_file presence and file permissions)
- Authentication/session policy: AllowRootLogin, MaxLoginRetry, idle/disconnect timeouts
- Listener exposure (0.0.0.0 bind, port) and Fork/session-isolation settings
- Secrets masked, CWE+ATT&CK mapping and TXT/MD/JSON/CSV/SARIF export with --fail-on gating

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage


```bash
./OXrdpX --scan -f sarif -o xrdp.sarif
./OXrdpX --xrdp /etc/xrdp/xrdp.ini --sesman /etc/xrdp/sesman.ini
./OXrdpX -r /mnt/image --fail-on high --json
./OXrdpX --demo
./OXrdpX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled.s.Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
