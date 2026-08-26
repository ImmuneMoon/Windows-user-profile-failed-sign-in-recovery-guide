# README: Universal Windows Profile & App Recovery Guide

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
