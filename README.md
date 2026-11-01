# Headuck F-Droid repository

The F-Droid software repository for **小鴨幹線 / HeaDuck Call blocker**
(`com.headuck.headuckblocker.dev`), published at:

```
https://repo.headuck.com/fdroid/repo
```

Add it to F-Droid by opening the link below, or by pasting the URL into
F-Droid → Settings → Repositories:

```
https://fdroid.link/#https://repo.headuck.com/fdroid/repo?fingerprint=52F43634B1A568447094597567564AFF677292B670B7CC703CB73E2694C37CC7
```

Repository signing key fingerprint:

```
52F43634 B1A56844 70945975 67564AFF 677292B6 70B7CC70 3CB73E26 94C37CC7
```

## Contents

```
fdroid/repo/          the published repository
├── index.xml, index-v1.jar, index-v1.json, index-v2.json, entry.json/jar
├── index.html        F-Droid's generated web listing
├── *.apk             released builds
├── icons/, icons-*/  app icons for the F-Droid client
├── diff/             incremental index updates
└── com.headuck.headuckblocker.dev/   per-app metadata and localised icons
index.html            redirects to /fdroid/repo/
```

The `/fdroid/repo/` prefix is part of the repository address and is referenced
by every configured client, so the file layout must not be reshuffled.

## About the files

Everything under `fdroid/repo/` is generated and signed offline by the
maintainer with `fdroid update`, using a key that is **never** stored in this
repository. This repo only mirrors those signed bytes so they can be served
over HTTPS — nothing here is built, rewritten or re-signed.

Never commit signing keys, keystore files or store credentials. Rotating the
signing key would change the fingerprint above and force every existing user to
re-add the repository, so it stays fixed.
