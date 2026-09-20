# Paquetería Ya Operations

Official Android downloads for the Paquetería Ya staff and driver app.
This repository contains distribution information and downloadable builds only.
Application source code is maintained privately.

## Current iOS QA — TestFlight 1.0.0 (20)

Existing internal testers can install **1.0.0 (20)** through their existing
TestFlight invitation. Apple confirms this build is valid and in internal beta
testing. Use the **QA account**; sign out before switching from production.

Includes the current QA printer pages, MC240 discovery/setup, separate receipt
and label defaults, 4×6 stock selection and full-size package-label correction.
Open **Printers → Add printer → Bluetooth label printer (MC240)**. Select 4×6,
print one test once, then print one actual package label. Check size, orientation,
QR scanning and the number of physical labels fed. iOS MC240 hardware testing is
still required; the owner-reported extra blank feed on Android remains unresolved.

The iOS archive, signing, QA configuration and native modules were verified.
No backend/schema change or migration is required. No public IPA or App Store
production release is included; existing internal TestFlight access is retained.

## Current Android QA — build 24

**[Download QA build 24 — full-size 4×6 package labels](https://github.com/paqueteria-ya/operations/releases/tag/v1.0.0-qa.24)**

[Direct APK download](https://github.com/paqueteria-ya/operations/releases/download/v1.0.0-qa.24/paqueteria-ya-operations-android.apk)

Corrects package content printing at 75% size on 4×6 shipping labels. The print
layout now uses physical points throughout. The existing QA printer discovery,
setup, separate receipt/label defaults and 4×6 stock selection are retained.

Use a QA/test account. Select **Printers → your MC240 → Label size → 4 × 6 in**,
then print one package once. Check full-size content, scan the QR and count labels.
Software tests and rendered PDF pagination pass; this build still needs a physical
retest. The previously reported complete extra blank label after the test pattern
is a separate unresolved issue. No automatic print retry has been added.

Signed standalone APK, no Metro or Expo Go. Sign out before switching from
production; it replaces the same Operations app. Installation/upgrade and iOS
hardware checks remain pending; no iOS installer is included. No backend or
schema change or migration is required.

## Previous Android QA — build 23

**[Download QA build 23 — MC240 4×6 default](https://github.com/paqueteria-ya/operations/releases/tag/v1.0.0-qa.23)**

[Direct APK download](https://github.com/paqueteria-ya/operations/releases/download/v1.0.0-qa.23/paqueteria-ya-operations-android.apk)

New MC240 setup defaults to **4 × 6 in (approximately 102 × 152 mm)**. For a saved
printer, open **Printers → your MC240 → Label size** and select 4 × 6 in. Existing
saved choices are preserved until you change them; 100 × 150 mm remains available.
The existing QA printer page, receipt discovery and separate defaults remain.

Print one test once. The frame and bars are intentional; check that exactly one
label comes out and no complete blank follows. An owner reported an extra blank
label with build 22. **Its cause and a physical fix remain unconfirmed.** If it
continues with matching stock, compare the same size/roll in MUNBYN Print. No
automatic retry or speculative feed command has been added.

Signed standalone QA APK; no Metro or Expo Go. Use a QA/test account. Sign out
before switching from production; this replaces the same Operations app. Software
checks passed; build 23 device retest and installation/upgrade checks are pending.
No iOS installer is included.

## Previous Android QA — build 22

**[Download QA build 22 — current QA app with MC240](https://github.com/paqueteria-ya/operations/releases/tag/v1.0.0-qa.22)**

[Direct APK download](https://github.com/paqueteria-ya/operations/releases/download/v1.0.0-qa.22/paqueteria-ya-operations-android.apk)

This includes the current selected QA mobile interface and its existing printer
setup, discovery and saved-printer system, with MC240 label printing added.
Existing Bluetooth and Wi-Fi receipt printers are retained.

Use a **QA/test account**. Open **Printers → Add printer → Bluetooth label printer
(MC240)**. Select stock, print the test frame and confirm the physical result before
saving. Receipt and label defaults are separate. Then open a QA package → Print
label → choose the saved MC240. Check the label edges and scan the package QR.

Standalone signed APK; no Metro or Expo Go. Sign out before switching from
production because this replaces the same Operations app. Physical-device install,
upgrade and printer testing remain pending. Data receipt does not prove a label
printed; interrupted jobs are never automatically resent. No iOS build is included.

This replaces build 21's older main-based interface. Build 21 remains below as
historical evidence; use build 22 for testing the combined QA printer system.

## Previous MC240-only test — build 21 (superseded)

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

Historical iPhone receipt-testing build: **1.0.0 (19)** in TestFlight.
Use the current iOS build 20 above for MC240 testing.
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
