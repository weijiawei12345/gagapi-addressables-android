# gagapi-addressables-android

Gagapi Unity Addressables remote content for **Android**.

## Remote.LoadPath (important)

jsDelivr returns **HTTP 403** for files over ~20MB. Use commit-pinned GitHub raw:

`https://raw.githubusercontent.com/weijiawei12345/gagapi-addressables-android/50c2b8c/`

After each content release, pin Remote.LoadPath to the commit that contains the bundles, rebuild Addressables, then push the new catalog.
