# Sift privacy policy

**Effective 2026-10-04. Applies to Sift 1.0 and later.**

This is the complete policy. Host this file as-is at a public URL and put that URL in the Play Console and on Sift's
store listing. The app's own Settings > Data and privacy screen shows a short summary of the points below (what Sift
can access, your history, export, delete); it does not reproduce this text.

## The short version

Sift looks at the apps on your phone so you can see what they can reach. Everything it finds stays on your phone.
Sift has no Internet permission, no account, no servers, no analytics, no ads and no crash reporting. Nobody, including
the people who make Sift, can see your results unless you send them yourself.

## What Sift reads on your phone

To audit your apps, Sift reads:

- **The list of installed apps** and, for each one, its name, version, install and update dates, the permissions it
  asks for and the ones you allowed (camera, microphone, location, contacts, files and media, SMS, calendar, body
  sensors).
- **The apps' installation files**, read only, to look for the names of known tracker SDKs in their code. Sift never
  runs code from other apps and never changes their files.
- **Usage access, if you allow it:** when each app was last used, whether it ran in the background, and when it ran a
  foreground service. You can say no; Sift then works in a reduced mode.
- **Enhanced monitoring, if you set it up:** which app used the camera, microphone or location, and when. This needs
  Shizuku or a one-time adb command that you run yourself.

Sift never reads the content of other apps: no photos, messages, files, audio, contacts or location. It sees *that* an
app used the microphone, never what it heard.

## What Sift stores

Sift stores its results in its own private storage on your phone, which other apps cannot read:

- the list of apps, their permissions, risk scores and tracker findings;
- the activity history (kept for 90 days by default; you can choose 30, 60, 90 or 180 days);
- your alerts, rules and the changes you made with Sift (so you can undo them);
- your settings.

Android's backup and phone-to-phone transfer are turned off for Sift, so none of this is copied to your Google
account or moved to a new phone.

## What leaves your phone

Only what you send, when you send it. Sift can create:

- a CSV of your activity log,
- a PDF or a text summary of your weekly report,
- a text summary of one app's report,
- a backup of your settings and rules (no history).

Each one opens the Android share sheet or file picker, and you choose where it goes. Sift does not send it anywhere
else.

If you tap "Email support", Sift opens your own email app with an empty message to `support@sift.app`. Sift attaches
nothing and does not send anything itself; whatever you attach, you write and send yourself. Sift does keep a small
local log of its own errors, switched off by default, and it deliberately records only what went wrong in general
terms — it does not contain your app list, app names or any of the data Sift reads about other apps. You can read it
before sending anything. We use what you send only to answer you.

## What Sift never does

- It never connects to the Internet. Android settings show that Sift has no Internet permission.
- It never shares, sells or rents data. There is no data to share: it never leaves your phone.
- It never shows ads and includes no advertising, analytics or crash-reporting code.
- It never uses your camera, microphone, location, contacts or other sensors itself.
- It never uninstalls an app or changes a permission without you: Android asks you to confirm, or, with Enhanced
  monitoring, you tap the change and can undo it. With Shizuku, a rule you set to "Notify and revoke" removes a
  permission by itself; each of those changes is shown in an alert you can undo.

## Permissions Sift uses

This is the complete list of permissions in Sift 1.0. Sift asks for nothing else, and never for Internet access.

| Permission | What it is for |
|---|---|
| See all installed apps (`QUERY_ALL_PACKAGES`) | To audit every app, including ones installed later. |
| Usage access (you choose) | To see when apps were used, which ran in the background, and which ones are unused. |
| Notifications (you choose) | To show alerts, the daily digest and the guard notification. |
| Run a foreground service (`FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_SPECIAL_USE`) | Sift guard, when you turn it on. |
| Run at startup (`RECEIVE_BOOT_COMPLETED`) | To restart the guard and the scheduled scans after a reboot or an update of Sift itself. |
| Ask to uninstall apps (`REQUEST_DELETE_PACKAGES`) | So "Uninstall" can open Android's confirmation. Sift never uninstalls anything by itself. |
| App-op statistics (`GET_APP_OPS_STATS`, only if you grant it, with adb or Shizuku) | Enhanced monitoring: which app used the camera, microphone or location, and when. Android never grants this by installing Sift. |
| Keep the phone awake (`WAKE_LOCK`) | Declared by the background scheduler Sift uses, so a scheduled scan can finish. |
| Talk to Shizuku (`moe.shizuku.manager.permission.API_V23`, only if you run Shizuku) | Changing another app's permission when you tap it, with Undo. |
| Sift's own internal permission (`DYNAMIC_RECEIVER_NOT_EXPORTED_PERMISSION`) | A signature-level permission that makes sure only Android and Sift can send messages to Sift's background parts. |

## Other apps and services

- **Shizuku** is a separate app you may install to turn on Enhanced monitoring. It has its own privacy policy.
- **Google Play and Android** handle installs, updates and system settings under Google's privacy policy. Sift cannot
  see or change what they collect.

## Children

Sift is not designed for children and does not knowingly process anything about them. It stores nothing off the
phone, for anyone.

## Your choices

- **Turn things off.** Usage access, notifications, Enhanced monitoring and Sift guard can each be turned off at any
  time in Android settings or in Sift.
- **Export.** Settings > Data and privacy > Export activity log.
- **Delete.** Settings > Data and privacy > Delete all Sift data removes history, rules and settings from the phone.
  This cannot be undone.
- **Uninstall.** Uninstalling Sift removes everything it stored.

## Changes to this policy

If Sift ever changes what it reads or stores, this policy changes first, the update notes say so, and the effective
date at the top changes. Sending anything off the phone would need the Internet permission, which Sift does not
have.

## Contact

Questions about this policy: **support@sift.app**.
