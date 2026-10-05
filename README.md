<img src="icon.png" width="96" alt="Sift">

# Sift

**An offline privacy auditor that shows what every app on your phone can
reach — and lets you close the gaps.**

Sift reads the permissions on your phone and explains them in plain language:
which apps hold your microphone, which can see your location all day, which can
reach your camera in the background. It scores the risk, tells you which ones
matter, and closes them for you. Everything it finds stays on your phone.

**[Privacy policy](privacy-policy.md)**

---

## Download

Sift is not on the Play Store yet. Until it is, you can install it directly.

**[Download the APK for v1.0.0 →](https://github.com/quillmatick/sift/releases/download/v1.0.0/sift-1.0.0-release.apk)**

Older versions stay available on the [releases page](https://github.com/quillmatick/sift/releases).
Each release is signed with the same key, so a newer version installs over an
older one and keeps your history, rules and settings.

<details>
<summary>How to install an APK on Android</summary>

<ol>
<li>Open the link above on your phone and download the file.</li>
<li>Android will warn you that the file came from outside the Play Store. This
is expected — tap <b>Settings</b>, then <b>Allow from this source</b>.</li>
<li>Open the downloaded file and tap <b>Install</b>.</li>
</ol>

<p>You may need to enable <b>Install unknown apps</b> for whichever app you used
to open the download (Chrome, Files, or your browser). It is a per-app setting
and you can turn it back off afterwards.</p>

</details>

**Requires Android 8.0 (API 26) or newer.** The APK is 3.7 MB.

---

## What it does

- **Explains every permission** — not a list of permission names, but what each
  one actually lets an app do and whether that is expected of it.
- **Scores risk per app** — a single number, with the reasons behind it, so you
  can judge the call yourself.
- **Closes gaps in one tap** — revoke a permission, with **Undo** if you change
  your mind.
- **Watches for background use** — set a rule once ("tell me if the mic is used
  while I'm not looking") and Sift tells you when it happens.
- **Explains the data it sees** — history, export to CSV, delete everything.
  Your activity log is kept for as long as you choose and is never sent anywhere.

## Two levels of monitoring

Sift works on its own out of the box. There is an optional second level if you
want it.

**Standard** — needs nothing but Usage access, which you grant in Android
settings. Sift reads the activity Android already records, so it can tell you
*what happened*, but it works from a snapshot rather than live.

**Enhanced** — uses [Shizuku](https://github.com/RikkaApps/Shizuku), a free app
that hands Sift Android's own permission tools. With it Sift can:

- watch sensor use **as it happens**, not just after the fact;
- change other apps' permissions **directly**, instead of sending you to system
  screens one at a time.

Shizuku is optional, separate, and off by default. It never gives Sift the
Internet — Sift does not request that permission at all, on either level.
Turn it off any time in Settings.

## What it does not do

- **No Internet permission.** Sift does not request it, so it cannot send your
  data anywhere even if it wanted to. A build check fails if that ever changes.
- **No account, no servers, no analytics, no ads, no crash reporting.**
- **It never sees your photos, messages, files or audio** — only whether an app
  asked for the ability to reach them.

## Status

This is an early release. It is a working build, not a finished product: the
Play Store version is not submitted yet, and some screens have not been checked
on tablets or on Android versions older than 15. The source is developed in
public and the known gaps are written down rather than hidden.

---

## Feedback

Found something wrong, or something Sift gets wrong about your phone? Open an
issue. Bug reports with the phone model and Android version are genuinely useful
here.