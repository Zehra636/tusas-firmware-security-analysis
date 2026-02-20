# TUSAŞ Firmware Security Analysis

## Project Overview

This project focuses on performing security analysis on an embedded Linux-based firmware image.

The analysis includes:

- Firmware integrity verification (SHA256 hash validation)
- WSL & Ubuntu environment setup
- Firmware extraction using Binwalk
- SquashFS filesystem analysis
- User account and authentication review
- Web interface security assessment
- Automated Python-based analysis prototype

---

## 1. Firmware Integrity Verification

The firmware file was verified using SHA256 hash comparison via Windows CertUtil tool.

Hash values matched the official reference, confirming file integrity. :contentReference[oaicite:0]{index=0}

---

## 2. Analysis Environment Setup

- WSL (Windows Subsystem for Linux) enabled
- Ubuntu 22.04 installed
- Required packages updated and fixed (Hash Sum Mismatch resolved)
- Tools installed:
  - binwalk
  - squashfs-tools
  - python3

---

## 3. Firmware Extraction

Firmware extracted using:


SquashFS filesystem successfully unpacked.

---

## 4. Filesystem Analysis

The extracted root filesystem included:

- /bin
- /etc
- /usr
- system configuration files

Indicating a Linux-based embedded OS.

---

## 5. Security Findings

### User Account Review

- /etc/passwd and /etc/shadow analyzed
- Root account locked
- Some shells disabled

Basic security hardening observed.

### Web Interface Vulnerability

- password.js transmits credentials in plain-text
- RPC authentication mechanism does not encrypt passwords
- Vulnerable to Man-in-the-Middle (MITM) attacks

This represents a critical security weakness.

---

## 6. Python Automated Analysis Tool

A Python prototype was developed to:

- Calculate SHA256 hash
- List extracted directories
- Generate static analysis outputs

The goal was to partially automate firmware inspection workflows.

---

## Skills Demonstrated

- Embedded Linux analysis
- Firmware reverse engineering
- Static security analysis
- Hash verification
- Vulnerability identification
- Python scripting
- Security mindset

---

## Author

Zehra
Adli Bilişim Mühendisliği Student
