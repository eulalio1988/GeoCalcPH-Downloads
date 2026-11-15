# GeoCalcPH SurveyTools — Installation & Activation Guide

GeoCalcPH SurveyTools is an AutoCAD plugin for geodetic engineers, surveying professionals, and students in the Philippines. The installer includes the OCR engine and its required models, so **OCR processing works offline after installation**. An internet connection is still required for online license activation and validation as described below.

## 1. System Requirements

- **Operating System:** Windows 7 or later (64-bit)
- **AutoCAD:** 2022, 2023, 2024, or 2025
- **.NET Framework:** 4.8 or later
- **RAM:** 4 GB minimum (8 GB recommended)
- **Free disk space:** At least 500 MB

## 2. Download

Download the official installer from the **Releases** section of this repository:

`GeoCalcPH_SurveyTools_Setup_v1.0.0.exe`

The installer is distributed as a single Windows executable. It includes the GeoCalcPH SurveyTools plugin and the bundled OCR engine/models.

> **Offline OCR:** You do not need to download OCR models separately. OCR functionality is available without an internet connection once installation is complete.

## 3. Install GeoCalcPH SurveyTools

1. Download `GeoCalcPH_SurveyTools_Setup_v1.0.0.exe` from the official GeoCalcPH release.
2. Close all running AutoCAD instances.
3. Double-click the downloaded EXE file. If Windows displays a security prompt because the installer is not signed with a commercial code-signing certificate, verify that you downloaded it from the official GeoCalcPH release and that its SHA-256 checksum matches the value published with the release.
4. Follow the installer prompts and complete the installation.
5. Start or restart AutoCAD.
6. Check that the **GeoCalcPH** ribbon tab is available.

The installer places the AutoCAD application bundle under the current Windows user's Autodesk ApplicationPlugins folder.

## 4. Verify the Installer (SHA-256)

Always verify the installer checksum after downloading it.

The SHA-256 checksum for this release is:

```text
5132EB1AEF6F26FD623EDFF8B04D93DF39358173B8912BAC6DFD24175721918E
```

To verify it using PowerShell, open PowerShell in the folder containing the downloaded installer and run:

```powershell
Get-FileHash ".\GeoCalcPH_SurveyTools_Setup_v1.0.0.exe" -Algorithm SHA256
```

Compare the `Hash` value returned by PowerShell with the checksum above. The values must match exactly. If they do not match, do not run the installer; download it again from the official release.

## 5. OCR and Offline Operation

GeoCalcPH SurveyTools includes its OCR engine and required OCR models in the installer.

- OCR processing is designed to work locally on the computer.
- OCR does not require an internet connection after installation.
- OCR models do not need to be downloaded separately.
- License activation and online license validation are separate from OCR processing and may require internet access.

## 6. License Activation

### Trial License

A 30-day trial may be requested or made available through the GeoCalcPH trial process, subject to the licensing system's approval and eligibility checks. Follow the instructions presented by the application or the official GeoCalcPH website.

### Activating a Purchased License

1. Open AutoCAD and locate the GeoCalcPH licensing tools.
2. Run the license activation command: `SURVEYLICENSEACTIVATE`.
3. Enter the license key supplied by GeoCalcPH.
4. Follow the prompts to complete activation.
5. Check the license status using `SURVEYLICENSESTATUS`.

Keep your license key private. Do not post it in public issues, screenshots, or support forums.

If activation fails, confirm that:
- The license key was entered correctly.
- The computer has an internet connection.
- Your firewall or security software permits HTTPS communication with `license.geocalcph.com`.

For assistance, contact `support@geocalcph.com`.

## 7. Online License Validation and Offline Use

License activation and validation are separate from the offline OCR feature.

- **Initial activation:** An internet connection is required to contact the license server.
- **Periodic validation:** The plugin may contact the license server to verify license status and seat usage.
- **Offline grace period:** Offline use is subject to the grace period configured for your license.
- **OCR operation:** OCR processing itself does not require an internet connection after the application and OCR resources have been installed.

Reconnect to the internet and restart AutoCAD if the application reports that license validation is required.

## 8. Troubleshooting

### GeoCalcPH ribbon tab does not appear

1. Close AutoCAD completely and reopen it.
2. Confirm that the installer completed successfully.
3. Check that the application bundle exists under:

   ```text
   %APPDATA%\Autodesk\ApplicationPlugins\GeoCalcPH.SurveyTools.bundle\
   ```

4. If the ribbon still does not appear, contact support and provide your AutoCAD version, Windows version, and any displayed error message.

### License activation or validation fails

1. Confirm that the computer is connected to the internet.
2. Check that HTTPS access to `license.geocalcph.com` is not blocked by a firewall or proxy.
3. Restart AutoCAD and check the license status again.
4. If the problem continues, contact `support@geocalcph.com`. Include the error message, AutoCAD version, and Windows version. Do not send your full license key; provide only the minimum identifying information requested by support.

### OCR does not work

1. Confirm that GeoCalcPH SurveyTools installation completed successfully.
2. Restart AutoCAD and try the OCR operation again.
3. Check whether your antivirus or endpoint security software quarantined or blocked files installed with GeoCalcPH.
4. If the problem persists, contact support and include the error message and a description of the OCR operation you were performing.

## 9. Uninstalling

Use **Windows Settings > Apps > Installed apps** (or **Apps & features** on older Windows versions) to locate and uninstall GeoCalcPH SurveyTools, if it is listed there.

If you cannot find the application in the installed-apps list, contact GeoCalcPH support for the appropriate removal instructions.

Do not manually delete the GeoCalcPH license-data folder unless you intend to remove the locally stored license information as well.

## 10. Support

- **Website:** https://geocalcph.com/
- **Support email:** support@geocalcph.com

When contacting support, include:
- AutoCAD version and build number
- Windows version
- GeoCalcPH SurveyTools version
- The exact error message or a screenshot
- The steps that reproduce the problem

Never include your full license key or other confidential credentials in a public post.

---

**Product:** GeoCalcPH SurveyTools  
**Release:** v1.0.0  
**Installer:** `GeoCalcPH_SurveyTools_Setup_v1.0.0.exe`  
**Copyright:** © 2026 GeoCalcPH. All rights reserved.
