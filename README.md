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

Offline remote-desktop server configuration auditor — xrdp / sesman / TigerVNC / x11vnc / TightVNC

---

## ✨ Features

- Stdlib INI parser for xrdp.ini / sesman.ini with line tracking, duplicates and typo detection
- xrdp — security_layer, crypt_level, TLS certificate & key analysis (DER parser: expiry, key size, sig alg, self-signed), ssl_protocols, tls_ciphers, channels, hard-coded session credentials, VNC back-end pivots
- sesman — AllowRootLogin, MaxLoginRetry, group gating, alternate shells, clipboard restriction, idle limits, Xorg/Xvnc params, SessionVariables, FUSE umask
- VNC — TigerVNC config (key=value & legacy perl), service / script / x11vncrc argument parsing, SecurityTypes, localhost, blacklist lockout, -nopw, -passwd, -unixpw, hook commands, websockify / noVNC, xstartup
- VNC password files decrypted offline (stdlib DES) and checked for blank / weak / reused view-only passwords
- Secrets masked everywhere; --root discovery; CWE + MITRE
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Self-test --demo, CI gates --fail-on / --min-severity

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OXrdpX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
