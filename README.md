# Paquetería Ya Operations

Official Android downloads for the Paquetería Ya staff and driver app.
This repository contains distribution information and downloadable builds only.
Application source code is maintained privately.

## Internal QA beta — printer testing

**[Download Android QA build 19](https://github.com/paqueteria-ya/operations/releases/tag/v1.0.0-qa.19)**

[Direct APK download](https://github.com/paqueteria-ya/operations/releases/download/v1.0.0-qa.19/paqueteria-ya-operations-android.apk)

This build uses the **isolated QA environment**. Sign in with a QA/test account.
It adds broader Bluetooth printer discovery, the POS XP-P1 BLE connection profile,
58/80 mm paper choices and confirmation of a readable test before saving a printer.
Physical printer compatibility still needs testing.

For iPhone, existing internal testers can install **1.0.0 (16)** in TestFlight.
That build also uses QA; GitHub does not provide an iPhone installer.

Sign out before switching from production. QA and production share the same
Android app ID; installing this APK replaces the current app. Downloads are
public, while access to company records requires an authorized app account.

## Production Android beta — unreleased software

There is no stable release yet. Builds marked **Pre-release** are for testing.

**[Download the Android beta — build 18](https://github.com/paqueteria-ya/operations/releases/tag/v1.0.0-beta.18)**

[View all builds](https://github.com/paqueteria-ya/operations/releases)

The production beta (build 18) connects to **production**. Sign in with your production
account; changes affect real business records. Download access does not grant
access to business records.

### Install

1. If the QA app is installed, sign out first. This beta replaces that app.
2. Open the beta page on your Android phone or tablet and download the `.apk` asset.
3. Open the downloaded file. If Android prompts, allow installation from your browser.
4. Finish installation, open Paquetería Ya, and sign in with your production account.

Updates currently require downloading and installing a newer APK manually.
Only Android APKs are available here for now.

### Verify a download

Each build includes `SHA256SUMS` to verify the APK file. Future builds receive
separate versioned pre-releases; previously published APKs are not overwritten.
