# Cotorie / コトリエ GitHub Pages版

このフォルダの中身を、そのままGitHubリポジトリへアップロードできます。

## 初回セットアップ

1. GitHubで新しいリポジトリを作成
2. このZIPを展開して、中身をすべてリポジトリへアップロード
3. リポジトリの `Settings` → `Pages`
4. `Build and deployment` の Source を `Deploy from a branch` にする
5. Branch を `main`、Folder を `/ (root)` にして Save
6. 数分待つと GitHub Pages のURLが発行されます

## 今後の更新方法

新しいHTMLを、次のような名前で追加するだけです。

- index_v1.html
- index_v2.html
- index_v3.html
- index_v4.html

GitHub Actions が一番数字の大きいファイルを自動で見つけて、
それを `index.html` にコピーします。

つまり普段は `index.html` を手で置き換える必要はありません。

### 例

現在:
- index_v1.html
- index.html

更新時:
- `index_v2.html` を追加して Commit

すると自動で:
- `index_v2.html` の内容 → `index.html`

に更新され、GitHub Pagesにも反映されます。

## 大事

- ファイル名は `index_v数字.html` 形式を推奨します。
- `index(1).html` 形式ではなく `index_v2.html` のようにしてください。
- GitHub Actions の実行には、リポジトリの Actions が有効である必要があります。
- Actions が `git push` できない場合は、`Settings` → `Actions` → `General` → `Workflow permissions` で
  `Read and write permissions` を許可してください。
- 現在の試作版には本物の決済・本人確認・音声配信・DBは接続していません。
