# gagapi-addressables-android

Gagapi Unity Addressables remote content for **Android**.

## Remote.LoadPath

`https://raw.githubusercontent.com/weijiawei12345/gagapi-addressables-android/aa-android-latest/`

Do **not** use jsDelivr for this repo — files over ~20MB get HTTP 403.

## Publish steps

1. Build Addressables in Unity (profile Remote.LoadPath = tag URL above)
2. Copy `ServerData/Android` into this repo and push `main`
3. Move tag: `git tag -f aa-android-latest && git push -f origin aa-android-latest`
