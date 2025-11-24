# AtlasLock

(Official website) https://atlaslap.com

Secure folder-to-archive encryption for Windows.  
Turn any folder into a single protected `.atlas` file.  
**Runs locally · No cloud · No telemetry.**

<img width="460" height="412" alt="A" src="https://github.com/user-attachments/assets/4f7d692e-c786-488c-8e96-4b8f1abb15d4" />

> This repository provides public information, screenshots and issue tracking.  
> The **source code is private** and is not included in this repository.

---

# Overview

**AtlasLock** is a modern Windows encryption tool that converts any folder into a single encrypted `.atlas` archive.  
It is built to be clean, predictable and user-friendly — without cloud services, accounts or unnecessary complexity.

Unlike traditional “password-protected ZIP/RAR” archives, AtlasLock uses **proper encryption**, safe defaults and a contemporary security model.

---

# Security (10/10)

AtlasLock follows a defense-in-depth approach based on modern, well-established cryptographic principles.  
Internal implementation details are intentionally not exposed.

- **Strong password protection**  
  Passwords are processed with a modern, memory-hard KDF (Argon2 family), significantly increasing brute-force cost.

- **Authenticated encryption**  
  The entire archive is encrypted using an AEAD construction, ensuring confidentiality and **tamper detection**.

- **Per-archive randomness**  
  Each `.atlas` file uses its own random salt and unique derived key material.

- **Protected metadata**  
  Both file contents and structural metadata are validated to prevent silent corruption or manipulated archives.

- **Streaming encryption architecture**  
  Large folders are processed in a streaming fashion without loading everything into memory at once.

- **Local-only cryptography**  
  All operations happen on the user’s machine. AtlasLock does not upload files, keys or analytics.

In short, AtlasLock behaves like a dedicated encryption system — not a themed ZIP.

---

# How it works

### **1. Locking a folder**
- Select the folder  
- Enter your password  
- AtlasLock compresses + encrypts everything into a single `.atlas` file

### **2. Unlocking**
- Open an existing `.atlas` archive  
- Enter the correct password  
- The original folder structure is restored

No cloud dependencies, no background syncing — everything is offline.

---

# Features

- One-click folder → `.atlas` conversion  
- Clean, lightweight Windows interface  
- Integrated compression + encryption  
- Safe cryptographic defaults  
- Predictable performance on large folders  
- Corruption detection and recovery safeguards  
- Designed with reliability and simplicity in mind  
- “Made in Greece” — single-developer project with no telemetry

---

# System Requirements

- **OS:** Windows 10 / Windows 11 (64-bit)  
- **Admin rights:** Not required  
- **Internet:** Not required for normal use  

---

# Download

Official installers and builds are available on the website:

Website https://atlaslap.com

Support support@atlaslap.com
