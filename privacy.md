---
title: Privacy Policy
permalink: /privacy
---

# Privacy Policy — Antivirus Cleaner

**Last updated: November 2, 2026**

---

## 1. Overview

Antivirus Cleaner ("the App", package `com.magic.apps.antivirus.cleaner`) scans the apps and files on your Android
device for known malware, warns you about apps with risky permission combinations, checks links and can block
dangerous websites. This Privacy Policy explains what data the App processes, what leaves your device and why.

The App is developed and maintained by an independent developer ("we"). The App has no user accounts, shows no ads and
does not sell data.

**Short version:** scanning happens entirely on your device. Your files, file names, the list of your apps and scan
results are never uploaded. Websites you visit and links you check are never uploaded either. The App sends only usage
statistics and crash reports (Firebase) and downloads database updates.

---

## 2. Data processed only on your device

| Data | Why | Leaves the device? |
|---|---|---|
| Contents of files in shared storage | Computing file hashes (MD5/SHA-1/SHA-256) and comparing them with the local signature database | **No** |
| File names and paths | Showing scan results, quarantine and the trusted list | **No** |
| List of installed apps, their permissions, install source and APK files | Scanning apps for malware, risk scoring, App audit, tracker detection | **No** |
| App usage times (only if you grant Usage access) | "Last used" and "Unused apps" in App audit | **No** |
| Scan history, activity log, trusted list, quarantined files, settings | App features | **No** |
| Addresses of websites your apps open (only while Web protection is on) | Comparing each site name with the local list of dangerous sites and blocking dangerous ones | **No** |
| Text of notifications from other apps (only if you turn on link protection for messages and grant Notification access) | Finding links in incoming messages and checking them against the local list | **No** |
| Links you paste into Link check | Checking the link against the local lists | **No** |

Quarantined files are moved to the App's private storage and are deleted automatically after 30 days or when you
uninstall the App. Uninstalling the App deletes all data listed above.

---

## 3. Data collected automatically

The App uses **Firebase Analytics** and **Firebase Crashlytics**, services provided by Google LLC.

- **Usage analytics:** which screens are opened and which features are used, for example "quick scan finished:
  324 files, 0 threats", "threat removed from a notification", "realtime protection turned on". Events contain counts
  and types. They never contain file names, file paths, file contents, website addresses or the list of your apps.
- **Threat actions:** when you remove, quarantine, restore, trust or untrust an item the App flagged, the event also
  contains the package name of that app or the SHA-256 hash and extension of that file, the detection type and risk
  score. This helps us find false positives and improve detection. It does not include file names or paths.
- **Crash reports:** when the App crashes or hits an error, a report is sent with the stack trace, device model,
  Android version, App version and the App's state at that time.
- **Identifiers:** Firebase assigns a random app-instance / installation identifier. The App does **not** use the
  Android advertising ID and does not link data to your identity.

This data is processed by Google in accordance with Google's Privacy Policy: https://policies.google.com/privacy.
Analytics and crash reporting are disabled in development builds.

---

## 4. Network connections

The App connects to the internet only to:

1. **Download database updates** (malware signatures, the list of dangerous sites and links, the list of known safe
   apps) from our GitHub repository (`github.com/magicapps-coder/antivirus-db`, `raw.githubusercontent.com`) and, if
   that is unavailable, signature databases from a public upstream mirror on GitHub Pages (`github.io`), whose files
   are checked with a digital signature before use.
2. **Download tracker signatures** from Exodus Privacy (`reports.exodus-privacy.eu.org`) about once a week.
3. **Fetch configuration** (update intervals, database locations) from Firebase Remote Config.
4. **Ask Google Play Protect** for its status and list of harmful apps through Google Play services on your device
   (Tools tab).
5. Send analytics and crash reports (section 3).
6. Process purchases of the optional Premium subscription through **Google Play Billing**. Payment details are handled
   by Google; the App only receives the subscription status and purchase token from Google Play.

Web protection does **not** send your traffic anywhere: it runs a local VPN on your device that only looks at the
names of the sites your apps ask for. Dangerous names are blocked; all other requests go to your normal DNS server
exactly as without the App. No traffic passes through our servers (we have none).

These requests do not include any of the on-device data from section 2. Like any HTTPS request, they reveal your IP
address to the server that answers them.

---

## 5. Permissions

| Permission | Purpose |
|---|---|
| All files access (`MANAGE_EXTERNAL_STORAGE`) | Read files in shared storage to scan them; move infected files to quarantine or delete them when you choose to. Optional: without it only apps are scanned. |
| Query all packages (`QUERY_ALL_PACKAGES`) | See every installed app in order to scan it for malware. |
| Foreground service, special use (`FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_SPECIAL_USE`) | Realtime protection: check newly installed apps and downloaded files. Shown as a persistent notification; can be turned off in Settings. |
| Notifications (`POST_NOTIFICATIONS`) | Alert you when a threat is found. |
| Run at startup (`RECEIVE_BOOT_COMPLETED`) | Restart realtime protection after the device reboots. |
| Usage access (`PACKAGE_USAGE_STATS`) | Optional, granted in system settings: show when apps were last used in App audit. |
| Request uninstall (`REQUEST_DELETE_PACKAGES`) | Open the system uninstall dialog for an app you chose to remove. |
| Internet, network state, wake lock | Database updates and background work. |
| Google Play Billing (`com.android.vending.BILLING`) | Buy and check the optional Premium subscription. |
| VPN service (`BIND_VPN_SERVICE`, granted in the system VPN dialog) | Web protection: a local VPN that blocks dangerous websites on the device. Optional, Premium. |
| Notification access (`BIND_NOTIFICATION_LISTENER_SERVICE`, granted in system settings) | Link protection for messages: check links in incoming notifications. Optional, Premium. |
| Battery optimization exemption (`REQUEST_IGNORE_BATTERY_OPTIMIZATIONS`) | Keep realtime protection running on devices that stop background apps. Asked only when you allow it. |

---

## 6. Data sharing

We do not sell, rent or share personal data with third parties. Data from section 3 is processed by Google as our
service provider.

---

## 7. Retention

On-device data is kept until you delete it in the App or uninstall the App (quarantined files: up to 30 days).
Firebase data is kept according to the retention settings of the Firebase project (crash reports: 90 days; analytics: 2 to 14
months, depending on the project settings).

---

## 8. Children's privacy

The App is intended for general audiences, including users aged 9 and older. It has no accounts, no chat or social
features, no ads and does not use the advertising ID. We do not knowingly collect personal information from children:
the only data that leaves the device is the anonymous usage statistics and crash reports described in section 3,
which contain no names, contact details, files or app lists. Parents or guardians who believe a child has provided
personal information can contact us (section 11) and we will delete it.

---

## 9. Security data sources

Signature data comes from ClamAV (GPLv2), ESET malware-ioc (BSD-2-Clause), abuse.ch MalwareBazaar and ThreatFox
(CC0), Sanesecurity, Echap stalkerware indicators (CC BY 4.0) and Amnesty International (CC BY 2.0). The list of
dangerous sites and links comes from URLhaus (CC0) and Phishing.Database (MIT). Tracker signatures come from Exodus
Privacy.

---

## 10. Changes to this policy

This policy may be updated from time to time. Changes are reflected by the date at the top of this page.

---

## 11. Contact

Questions about this policy: **victoramazon1001@gmail.com**
