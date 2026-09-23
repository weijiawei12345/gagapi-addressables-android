# gagapi-addressables-android

Gagapi Unity Addressables remote content for **Android** build target.

Synced from `ServerData/Android` in the Gagapi Unity project.

## Contents

- `catalog_*.json` / `catalog_*.hash` — Addressables catalogs
- `*.bundle` — remote AssetBundles (RemoteGroup, monsters, localization, etc.)

## Use as Addressables Remote.LoadPath

1. Prefer a CDN or static host in front of this repo (or make the repo public and use jsDelivr).
2. Example public CDN base URL:

```
https://cdn.jsdelivr.net/gh/weijiawei12345/gagapi-addressables-android@main/
```

3. In Unity Addressables profile `AndroidLocal`, set:

- `Remote.BuildPath` = `ServerData/Android` (local build output stays the same)
- `Remote.LoadPath` = the CDN / hosting base URL above (must end with `/`)

4. Rebuild Addressables content after changing `Remote.LoadPath` so the catalog embeds the new URLs.

## Local Hosting (dev)

Unity Hosting Service can still serve `ServerData/Android` on LAN for Editor/device testing.

## Update workflow

1. In Unity: Addressables **Build > New Build > Default Build Script**
2. Copy/sync new files from `ServerData/Android` into this repo
3. Commit and push

## Note

Binary bundles are stored in Git (largest files ~64MB, under GitHub's 100MB limit). Total size is ~520MB.
