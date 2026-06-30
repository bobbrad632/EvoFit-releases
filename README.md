# EvoFit — release channel

Public mirror that holds:

- `latest.json` — version metadata consumed by the in-app updater
- GitHub Releases tagged `v*` — signed APK assets for sideload install

Source code lives in the private `bobbrad632/EvoFit` repo. This mirror exists
so the unauthenticated app can fetch update metadata and APKs anonymously.

The in-app updater reads:

```
https://raw.githubusercontent.com/bobbrad632/EvoFit-releases/main/latest.json
```

Then verifies the downloaded APK with the `sha256` from `latest.json` before
launching Android's package installer.
