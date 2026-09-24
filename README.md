# gagapi-addressables-android

## Remote.LoadPath（热更新根地址，可变）

`https://raw.githubusercontent.com/weijiawei12345/gagapi-addressables-android/aa-android-latest/`

**禁止**把 LoadPath 钉死到 git commit --trailer "Co-authored-by: Cursor <cursoragent@cursor.com>" SHA。commit 不可变，无法追加新的热更 bundle / catalog。

## 正确热更流程

1. **底包**：Unity New Build（LoadPath = 上面 tag）→ 打 APK（settings.json 里 remote hash 必须是 `aa-android-latest`）
2. 改资源后：`Build → Update a Previous Build`，选底包对应的 `addressables_content_state.bin`
3. 上传 `ServerData/Android`（新 catalog + 新/变更 bundle）
4. `git tag -f aa-android-latest && git push -f origin aa-android-latest`

## 不要用 jsDelivr

单文件超过约 20MB 会 HTTP 403。
