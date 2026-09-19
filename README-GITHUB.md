# GitHubへのアップ手順（Webブラウザだけで完了）

**ZIPのままではアップできません。必ず先に展開してください。**

1. ZIPを展開（ダブルクリック／右クリック→「すべて展開」）。
2. GitHubで新しいリポジトリを作成（Public。README等は追加しない）。
3. 作成後の画面の **「uploading an existing file」** をクリック。
4. 展開したフォルダを開き、**中身（index.html、column、assets、images、audio など）をすべて選んで** ブラウザにドラッグ&ドロップ。
   - フォルダごとではなく、フォルダの「中身」を入れてください（`index.html` がリポジトリの一番上に来る形）。
   - ファイル数は29、最大ファイルは約11MBで、Webアップロードの上限（1回100ファイル・1ファイル25MB）に収まっています。
5. 「Commit changes」を押す。
6. **Settings → Pages → Build and deployment**
   - Source: **Deploy from a branch**
   - Branch: **main** / **(root)** → Save
7. 数分後、`https://<ユーザー名>.github.io/<リポジトリ名>/` で公開されます。

## 公開後に必要な設定
- `sitemap.xml`、`robots.txt`、各ページの canonical にある `https://YOUR-DOMAIN.example` を、公開URLに置き換えてください（テキスト検索置換で可）。
- 会員登録フォームは、公開URLから初回送信すると、ykfuruya0703@gmail.com にFormSubmitの有効化メールが届きます。リンクをクリックして有効化してください。

## 補足
- EP.07の音声は、アップ上限に収めるため、元より圧縮（AAC 96kbps）しています。
- コラム本文を編集・再生成するための `tools/` は、この一式には含めていません（別ZIPの `roasting-note-lp.zip` に入っています）。
