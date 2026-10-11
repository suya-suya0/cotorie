# Cotorie / コトリエ GitHub Pages版 v3（バグ修正版）

## 修正内容
- v2でJavaScript内のテンプレートに `<script>` を入れてしまい、ブラウザがそこで本体スクリプトを終了扱いしていた問題を修正
- アタメ用ユーザー情報を通常のJavaScript配列に変更
- Service Workerをv3に更新
- HTMLはネットワーク優先にして、GitHubへ更新した内容が古いキャッシュに負けにくいよう変更

## GitHubへの更新
このZIPの中身をリポジトリへ追加・上書きしてください。

特に追加される最新版:
- index_v3.html
- sw.js

既存のGitHub Actionsが動けば `index_v3.html` が自動で `index.html` に反映されます。

もし既に `index.html` もアップロードするなら、その時点ですぐv3の内容になります。

## スマホで古い壊れた画面が残る場合
1. GitHub Actions / Pagesの更新が終わるまで少し待つ
2. 一度ページを再読み込み
3. それでも古い場合は、ホーム画面に追加済みのコトリエを閉じて再度開く
4. 必要ならサイトデータ/キャッシュを削除
