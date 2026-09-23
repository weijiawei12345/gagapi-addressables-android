# gagapi-addressables-android

Gagapi Unity Addressables remote content for **Android**.

## Remote.LoadPath (Unity profile AndroidLocal)

```
https://cdn.jsdelivr.net/gh/weijiawei12345/gagapi-addressables-android@main/
```

Also used as Remote Catalog Load Path. After changing this URL, rebuild Addressables in Unity, then sync `ServerData/Android` here and push.

## Update workflow

1. Unity: Build > New Build > Default Build Script
2. Copy `ServerData/Android/*` into this repo
3. `git add -A && git commit --trailer "Co-authored-by: Cursor <cursoragent@cursor.com>" && git push`
