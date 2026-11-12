# TM Apps — F-Droid Repo by MD. Muklash Mia

An F-Droid-compatible repository for **TM Player** and **TM Sounds** — free,
ad-free, open-source Android apps by
[MD. Muklash Mia](https://github.com/Muklash-Dev). No gatekeeper, no review
queue: add this repo in the F-Droid app and both apps install and update
directly from here.

## Add this repo in F-Droid

1. Open the **F-Droid** app → **Settings → Repositories → +** (add repository).
2. Paste this address:

   `https://muklash-dev.github.io/fdroid-repo/repo`
3. Check the fingerprint matches this one before confirming:

   `64DF BEB5 0CEA D115 BF56 61AD 96CF 06C8 874F 8C98 7F15 0C2D B8CA FB01 0201 11E2`
4. Refresh — **TM Player** and **TM Sounds** appear in the app list.

## Apps in this repo

| App | Version | Android |
| --- | --- | --- |
| **TM Player** (`com.muklashdev.tmplayer`) — free video & music player, USB/SD/OTG scan, private vault | 0.1 (build 9) | 8.0+ |
| **TM Sounds** (`com.muklashdev.tmsounds`) — no-root sound enhancer, EQ curve, volume boost | 0.1 (build 1) | 8.0+ |

Sources: [TM-Player](https://github.com/Muklash-Dev/TM-Player) ·
[TM-Sounds](https://github.com/Muklash-Dev/TM-Sounds) ·
Contact: Telegram [@muklash_dev](https://t.me/muklash_dev)

## For the developer — publishing an update

The signing key (`keystore.p12`) and `config.yml` are **not** in this repo —
they stay private on the build machine. Lose them and every user has to
re-add the repo, so keep a backup.

1. Copy the new APK into `repo/` as `<package>_<versionCode>.apk`
   (e.g. `com.muklashdev.tmplayer_10.apk`).
2. Run `fdroid update` in the repo folder (regenerates the signed index).
3. Push only `repo/` and `metadata/` to this repo — GitHub Pages serves it.
   Never push `config.yml`, `keystore.p12`, `tmp/` or `srclibs/`.

Built with [fdroidserver](https://f-droid.org/docs/Setup_an_F-Droid_App_Repo).
