# 5品レシピ PWA

## ファイル
- `index.html`：アプリ本体
- `manifest.json`：ホーム画面追加用の設定
- `service-worker.js`：オフライン利用のためのキャッシュ
- `icon-192.png` / `icon-512.png`：アプリアイコン

## 公開方法（無料・GitHub Pagesの例）
1. GitHubで新しい公開リポジトリを作成します（例：`recipe-checklist`）。
2. このZIPを解凍し、中の5ファイルをリポジトリの一番上にアップロードします。
3. GitHubのリポジトリで Settings → Pages を開きます。
4. Build and deployment の Source を「Deploy from a branch」にし、Branchを `main`、Folderを `/(root)` にして Save。
5. 数分後に表示される `https://ユーザー名.github.io/recipe-checklist/` をAndroidのChromeで開きます。
6. Chrome右上の︙メニューから「アプリをインストール」または「ホーム画面に追加」を選びます（表示名は端末・Chromeの状態で異なります）。

## 注意
- PWAとしてホーム画面追加・オフライン利用するには、HTTPSで公開する必要があります。端末内のローカルHTMLを直接開いただけではService Workerが動作しません。
- チェック状態はブラウザのローカル保存です。同じURL・同じブラウザ内で保持されます。別端末とは同期されません。
- 公開リポジトリに個人情報を含めないでください。
