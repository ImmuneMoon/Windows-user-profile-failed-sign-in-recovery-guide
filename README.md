# README: Universal Windows Profile & App Recovery Guide

![Windows 10 | 11](https://img.shields.io/badge/Windows-10%20%7C%2011-0078D4?logo=windows&logoColor=white)
![Fixes temporary profiles and failed sign-ins](https://img.shields.io/badge/Fixes-temporary%20profile%20%7C%20failed%20sign--in-6f42c1)
![Tools: Registry Editor, SFC](https://img.shields.io/badge/Tools-Registry%20Editor%20%7C%20SFC-5c2d91)
[![Last updated](https://img.shields.io/github/last-commit/ImmuneMoon/Windows-user-profile-failed-sign-in-recovery-guide?label=updated)](https://github.com/ImmuneMoon/Windows-user-profile-failed-sign-in-recovery-guide/commits/main)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey)](LICENSE)

## 📖 Overview
The **Universal Windows Profile & App Recovery Guide** is a step-by-step troubleshooting manual designed to help users resolve the common Windows issue where a user profile becomes corrupted (often due to sudden power loss or system crashes), causing Windows to boot into a looping "Temporary Profile." 

This guide provides a reliable method to restore your original user profile without needing to reinstall the operating system or lose personal data.

## 🗂 Contents of the Guide
The main document (`Windows-Profile-Recovery-Guide.md`) is divided into three distinct phases:
1. **Phase 1: Breaking the Profile Loop via Registry Editor** - Steps to safely navigate the Windows Registry, locate your corrupted profile keys, and perform a registry swap to restore your original profile path.
2. **Phase 2: Resolving System File Inconsistencies** - Instructions for running the System File Checker (SFC) tool via an elevated Command Prompt to repair any underlying OS damage.
3. **Phase 3: Optional Universal App Cache Purge** - A quick method to reset specific applications that may be crashing or freezing due to residual corrupted data from the initial system failure.

## ⚠️ Important Disclaimer
**Proceed with caution.** Phase 1 of this guide requires modifying the Windows Registry (`regedit`). 
* Incorrectly modifying the registry can cause serious, system-wide issues. 
* Always ensure you are following the exact paths and modifying the correct keys as specified in the guide.
* It is highly recommended to back up the registry or create a System Restore point before beginning.

## 🚀 How to Use
Simply open the `Windows-Profile-Recovery-Guide.md` file in any Markdown viewer, text editor, or code editor (such as VS Code, Notepad++, or Obsidian) and follow the instructions sequentially from Phase 1 to Phase 3.

## ☕ Support the Project

If you find this project helpful and want to support further development by Fulllion Creative Works, consider leaving a tip!

* [Donate via PayPal](https://www.paypal.com/donate/?hosted_button_id=LCDZX75HR4CLC)
* [Support on Ko-fi](https://ko-fi.com/fulllion)

---
© 2026 Fulllion Creative Works. All rights reserved.

