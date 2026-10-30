# 📋 Universal Windows Profile & App Recovery Guide

![Windows 10 | 11](https://img.shields.io/badge/Windows-10%20%7C%2011-0078D4?logo=windows&logoColor=white)
![Fixes temporary profiles and failed sign-ins](https://img.shields.io/badge/Fixes-temporary%20profile%20%7C%20failed%20sign--in-6f42c1)
![Tools: Registry Editor, SFC](https://img.shields.io/badge/Tools-Registry%20Editor%20%7C%20SFC-5c2d91)
[![Last updated](https://img.shields.io/github/last-commit/ImmuneMoon/Windows-user-profile-failed-sign-in-recovery-guide?label=updated)](https://github.com/ImmuneMoon/Windows-user-profile-failed-sign-in-recovery-guide/commits/main)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey)](LICENSE)

**📄 [Download the PDF](Windows-user-profile-failed-sign-in-recovery-guide.pdf)**

## 📖 Overview
The **Universal Windows Profile & App Recovery Guide** is a step-by-step troubleshooting manual designed to help users resolve the common Windows issue where a user profile becomes corrupted (often due to sudden power loss or system crashes), causing Windows to boot into a looping "Temporary Profile." 

This guide provides a reliable method to restore your original user profile without needing to reinstall the operating system or lose personal data.

## ⚠️ Important Disclaimer
**Proceed with caution.** Phase 1 of this guide requires modifying the Windows Registry (`regedit`). 
* Incorrectly modifying the registry can cause serious, system-wide issues. 
* Always ensure you are following the exact paths and modifying the correct keys as specified in the guide.
* It is highly recommended to back up the registry or create a System Restore point before beginning.

## 🚀 How to Use
Download the PDF above, or read on below. Follow the instructions in order from Phase 1 to Phase 3.

---

<!-- guide:start -->

## Why This Happens
This issue is commonly triggered when an unexpected power drop (such as a thunderstorm outage) or an aggressive program hang abruptly cuts off a user registry hive while files are actively writing. Windows flags the user profile as corrupted on the next boot cycle and shunts your login sequence into a looping temporary path.

## Phase 1: Breaking the Profile Loop via Registry Editor
1. Boot into Windows. If you are permanently stuck on a flashing "Preparing Windows" interface, press and hold the machine's physical power switch for 10 seconds to force a deep shutdown, then launch into Safe Mode.
2. Press the `Windows Key + R` to prompt the Run field, input `regedit`, and hit **Enter**.
3. In the left panel directory tree, expand the folders to drill down into this exact path:
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\ProfileList`
4. Expand the `ProfileList` category folder and scan the bottom of the list for your unique account string keys (e.g., look for "twin folders" where one ends in `-1001` and the other ends in `-1001.bak`).
5. **Execute the Registry Swap:**
   * Right-click the folder without `.bak` (the one ending natively in `-1001`), select **Rename**, and append `.old` to the end of the text string.
   * Right-click the folder with `.bak` (the one ending in `-1001.bak`), select **Rename**, and carefully delete the `.bak` extension so it ends cleanly with just the profile numbers.
6. Click on your newly targeted clean folder. Look over at the right-side configuration pane:
   * Double-click the `State` item, change the Value data field to `0`, and click **OK**.
   * Double-click the `RefCount` item (if visible in your menu), shift its data value to `0`, and click **OK**.

## Phase 2: Resolving System File Inconsistencies
1. Click your Start menu icon, input `cmd`, right-click **Command Prompt**, and choose **Run as administrator**.
2. Input `sfc /scannow` and press **Enter**.
3. Allow the scanning utility to cross 100% verification to repair broken or open structural dependencies left behind by the sudden system power cuts.
4. Exit out of all panels and choose **Start > Power > Restart** to load back into your genuine profile workspace.

## Phase 3: Optional Universal App Cache Purge (For Any Broken App)
If you land safely on your authentic desktop background but find that a specific desktop application instantly locks up, crashes, or refuses to launch due to lingering "dirty" data blocks left behind by the power cut, you can clear its local data profile:

1. Press the `Windows Key + R` combination on your keyboard.
2. Input `%appdata%` into the empty Run dialog field and hit **Enter**.
3. In the folder that opens, look for the directory named after the software developer or the application itself (e.g., the name of the program that froze).
4. Right-click and **Delete** that specific application folder completely.
5. **Optional Second Location:** If you do not see the app name there, press `Windows Key + R` again, type `%localappdata%`, press **Enter**, and check for the folder there.
6. **Launch the software:** Windows will instantly rebuild a fresh, completely uncorrupted version of these directories the next time you fire up the application, clearing away any localized software glitches.

<!-- guide:end -->

## ☕ Support the Project

If you find this project helpful and want to support further development by Fulllion Creative Works, consider leaving a tip!

* [Donate via PayPal](https://www.paypal.com/donate/?hosted_button_id=LCDZX75HR4CLC)
* [Support on Ko-fi](https://ko-fi.com/fulllion)

---
© 2026 Fulllion Creative Works. All rights reserved.
