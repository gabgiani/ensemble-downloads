# Ensemble downloads

Apps and installers for **Ensemble**, a workspace where a team puts the 3D model, the drawing, the discussion and the plan in one place. Free for one user on your own devices.

- Website: https://ensemble.dafonet.com
- What it does: https://ensemble.dafonet.com/features.html
- Report a problem or ask for TestFlight: gabriel.giani@gmail.com

## Which file do I download?

| I use… | Download | Needs |
|---|---|---|
| Windows PC | `ensemble-setup_X.Y.Z_x64.exe` from the [server and Windows releases](https://github.com/gabgiani/ensemble-downloads/releases/latest) | Windows 10 or later, 64-bit. Choose “Ensemble only” unless this PC will host workspaces |
| Mac | `ensemble_X.Y.Z_macos-arm64.pkg` (or `.zip`) from the [Mac app releases](https://github.com/gabgiani/ensemble-downloads/releases?q=app-mac) | macOS 13 or later, Apple silicon |
| iPad or iPhone | TestFlight: [request an invite](https://ensemble.dafonet.com/download.html) | iPadOS or iOS with the free TestFlight app |
| Android phone or tablet | `ensemble-android_X.Y.Z_arm64.apk` from the [Android releases](https://github.com/gabgiani/ensemble-downloads/releases?q=android) | Android 10 or later, 64-bit ARM. Sideload |
| Meta Quest | `ensemble-quest_X.Y.Z_arm64.apk` (the app as a panel) and `ensemble-vr_X.Y.Z_arm64.apk` (VR viewer) from the [Android releases](https://github.com/gabgiani/ensemble-downloads/releases?q=android) | Quest 2, Pro, 3 or 3S. Sideload |
| A team server on my network | `ensemble-server_X.Y.Z_macos-arm64.pkg` (Mac) or the Windows installer with the server component, from the [server releases](https://github.com/gabgiani/ensemble-downloads/releases/latest) | Free software; see [on-premise](https://ensemble.dafonet.com/on-premise.html) |

## Installing

- **Windows:** run the installer. It is signed by DAFO AI LTD.
- **Mac:** open the `.pkg`. Both the app and the server are signed with a Developer ID and notarized by Apple.
- **iPad and iPhone:** install Apple’s TestFlight app, send us the email of your Apple ID, and accept the invite Apple sends you.
- **Android and Quest:** use `adb install -r file.apk`, or copy the file to the device, allow installs from that source and open it. These APKs are signed with a development key and are not on Google Play or the Meta Store. Each release has a `SHA256SUMS` file.

## All versions

Each version stays available. Notes are only as detailed as we can stand behind: versions before 0.3.0 were published without a changelog.

### 0.3.0 · 2026-11-08 · SolidWorks and AutoCAD files, free rotation, cleaner large models
- Opens SolidWorks parts (.SLDPRT) and complete assemblies (.SLDASM) straight from the file, with their structure and part names
- Opens AutoCAD DWG drawings (2013 format) as vector drawing cards, and the AI can propose a 3D model from them
- 3D viewer: you can now rotate all the way over and under a part, with no limit on the vertical turn
- 3D viewer: fixed the speckled, outlined patches that appeared on large assemblies when zoomed out (depth precision)
- Analysis works on SolidWorks parts and assemblies; interference check and exact comparison still need a STEP
- New builds: Meta Quest (VR viewer and the full app as a panel) and Android phones and tablets (sideloaded APK)
- Downloads: [Server and Windows](https://github.com/gabgiani/ensemble-downloads/releases/tag/v0.3.0), [Mac app](https://github.com/gabgiani/ensemble-downloads/releases/tag/app-mac-v0.3.0), [Android and Quest](https://github.com/gabgiani/ensemble-downloads/releases/tag/android-v0.3.0)

### 0.2.6 · 2026-11-07 · Server and Mac app update
- Ensemble Server 0.2.6 for macOS (Apple silicon) and Ensemble for Mac 0.2.6, signed and notarized
- Downloads: [Server](https://github.com/gabgiani/ensemble-downloads/releases/tag/v0.2.6), [Mac app](https://github.com/gabgiani/ensemble-downloads/releases/tag/app-mac-v0.2.6)

### 0.2.5 · 2026-11-07 · First release of the Mac app
- Ensemble for Mac 0.2.5 (Apple silicon, macOS 13 or later), signed with Developer ID and notarized
- Downloads: [Mac app](https://github.com/gabgiani/ensemble-downloads/releases/tag/app-mac-v0.2.5)

### 0.2.4 · 2026-11-06 · Server for macOS and Windows installer
- Ensemble Server 0.2.4 for macOS and the signed Windows installer
- Downloads: [Server and Windows](https://github.com/gabgiani/ensemble-downloads/releases/tag/v0.2.4)

### 0.2.1 · 2026-11-06 · First signed Windows installer
- Ensemble by DAFO 0.2.1 for Windows (x64), signed installer
- Downloads: [Windows](https://github.com/gabgiani/ensemble-downloads/releases/tag/v0.2.1)

## Checking a download

Every file has a SHA-256 in its manifest (`*.json` in this repository) or in the release. On a Mac or Linux: `shasum -a 256 file`. On Windows: `Get-FileHash file`.
