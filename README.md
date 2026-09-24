# gagapi-addressables-android

## Remote.LoadPath

`https://raw.githubusercontent.com/weijiawei12345/gagapi-addressables-android/aa-android-latest/`

## Hot update (Update a Previous Build)

1. Keep `Assets/AddressableAssetsData/Android/addressables_content_state.bin` from the player/base build
2. Unity: Addressables Groups → Build → Update a Previous Build → select that `.bin`
3. Upload changed `catalog_*.json` / `.hash` and new `*.bundle` files
4. `git tag -f aa-android-latest && git push -f origin aa-android-latest`

Do not pin LoadPath to a git commit --trailer "Co-authored-by: Cursor <cursoragent@cursor.com>" SHA — commits are immutable and cannot receive new update bundles.
