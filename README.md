# Cotorie v4 — 「コトリエを開く」ボタン修正版

## 原因
v3では、初回画面を隠すための `.hidden { display:none }` より後に
`.launch { display:flex }` が定義されていました。

CSSの優先順位上、`launch hidden` の両方が付いても後から書かれた
`display:flex` が勝ってしまい、ボタンを押しても初回画面が消えない状態でした。

## 修正
- `.hidden { display:none!important }` に変更
- Service Workerをv4に更新
- `index_v4.html` を最新版として追加

GitHubにはこのZIPの中身を追加・上書きしてください。
既存のActionsが動けば `index_v4.html` が自動で `index.html` に反映されます。
