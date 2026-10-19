# Shani Shvilin releases

Public releases of the Shani Shvilin Android app. The source code is not here.

- **Releases**: each tag `vX.Y.Z` (stable) or `vX.Y.Z-beta.N` (pre-release) carries
  `ShaniShvilin-<version>-arm64-v8a.apk`, `ShaniShvilin-<version>-armeabi-v7a.apk`,
  `ShaniShvilin-<version>-universal.apk` and `SHA256SUMS`.
- **`update/`**: what the app reads to update itself.
  - `stable.json`, `beta.json`: signed envelopes, `{"payload": <base64 manifest>, "signature": <base64 ECDSA P-256 SHA-256>}`.
    The app verifies the signature against the catalog key it pins, then installs only an APK signed with the
    same certificate as the installed app and with a higher versionCode.
  - `version.json`: an unsigned summary per channel, for the site and the installers.

Everything here is written by `tools/release-apk.sh` in the app repository. Do not edit by hand.

Installation guides: https://shanishvilin.abaye.co

© abaye. All rights reserved.
