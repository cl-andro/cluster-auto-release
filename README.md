# Cluster Auto - Release Repository

This repository contains the build workflow scripts, license, and instructions to download and install **Cluster Auto** — the background bridge manager daemon for the Cluster Family ecosystem on Android.

---

## 📥 How to Download & Install

1. Navigate to the **Releases** section on the right side of this GitHub repository page.
2. Download the latest `cluster-auto-release.apk`.
3. Transfer the APK to your phone and install it (make sure you allow installation from "Unknown Sources" in your browser/file explorer if prompted).

---

## 📦 About Cluster Auto

**Cluster Auto** (`com.zk.clAuto`) is the background bridge manager daemon that enables root/shell-level file system access for Cluster Family applications on Android.

### Key Features
- Root access bridge via Magisk, KernelSU, or APatch
- Shell-level access via ADB for non-rooted devices
- Automatic authorization for Cluster Family apps
- Native daemon with JNI for high-performance system operations

### 🔒 Pre-Authorized Applications
The following applications are automatically pre-authorized to connect to the daemon:
* `com.zk.clfiles` (Cluster Files)
* `com.zk.clandro` (CL-Andro)
* `com.zk.clbrowser` (CL-Browser)

---

## 🚀 Starting the Daemon Service

### Option A: Rooted Devices (100% Unrestricted Root Access)
1. Open the **Cluster Auto** app on your phone.
2. Tap **Start via Root**.
3. Grant **Superuser (Root)** access when prompted.

### Option B: Non-Rooted Devices (Shell-Level Access via ADB)
1. Connect your phone to your computer with a USB cable.
2. Open a terminal on your computer.
3. Run the following command:
   ```bash
   adb shell $(pm path com.zk.clAuto | cut -d: -f2 | sed 's/base.apk/lib\/arm64\/libclauto.so/')
   ```

---
*For questions or concerns, contact: zkalamgir@proton.me*
