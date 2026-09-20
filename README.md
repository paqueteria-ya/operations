# Paquetería Ya Operations

Official Android downloads for the Paquetería Ya staff and driver app.
This repository contains distribution information and downloadable builds only.
Application source code is maintained privately.

## MC240 label-printer QA test — build 21

**[Download MC240 Android QA build 21](https://github.com/paqueteria-ya/operations/releases/tag/v1.0.0-qa.21)**

[Direct APK download](https://github.com/paqueteria-ya/operations/releases/download/v1.0.0-qa.21/paqueteria-ya-operations-android.apk)

Use a **QA/test account**. Open a QA package → Print label → MUNBYN MC240.
Search, select the label stock, and print the test frame before sending package
labels. Check the paper and scan the QR. Data receipt does not prove physical
print completion, and interrupted jobs are never resent automatically.

This is a focused MC240 candidate based on the approved main app. It does **not**
include the QA-only receipt-printer features described for build 20 below. It
replaces the same Android app; sign out before switching from production. No Metro
server or Expo Go is needed. Physical MC240 compatibility and installation/upgrade
checks remain pending on real devices. This download does not include iOS.

## Receipt-printer QA test — build 20

**[Download Android QA build 20](https://github.com/paqueteria-ya/operations/releases/tag/v1.0.0-qa.20)**

[Direct APK download](https://github.com/paqueteria-ya/operations/releases/download/v1.0.0-qa.20/paqueteria-ya-operations-android.apk)

This build uses the **isolated QA environment**. Sign in with a QA/test account.
Build 20 tests a fix for slow receipt printing: removes per-chunk Bluetooth/Wi-Fi
pauses and negotiates larger BLE packets where supported. It retains the earlier
printer discovery, 58/80 mm settings and confirmed test before saving. Compare
paper-feed pauses, complete output and QR readability on your actual printers.

[Previous Android QA build 19](https://github.com/paqueteria-ya/operations/releases/tag/v1.0.0-qa.19)
remains available for reference. Install build 20 over build 19; older APKs are not
promised as in-place downgrades.

For iPhone, existing internal testers can install **1.0.0 (19)** in TestFlight.
This QA build streams Bluetooth data when the printer advertises support, with
queue backpressure and an acknowledged-write fallback. Build 17 still paused in
physical testing; build 19 needs the same test before speed is considered fixed.

Print the short Bluetooth test receipt and check timing, complete output and QR
readability. If it still pauses or loses output, open **Receipt printers → Share
last print details** and send the report with your printer model and observations.
The report contains timings and transfer counters, without receipt/account data.
Also compare a long receipt and your other compatible Bluetooth/Wi-Fi printers.

Open TestFlight using your existing internal tester invitation. GitHub does not
provide an iPhone installer. Native app builds and delivery do not use Vercel.

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
