# JPプロダクトリテイリング合同会社 会社概要サイト

JPプロダクトリテイリング合同会社の会社情報と取扱分野を、老舗美術商、古書店、版画店、作品整理中の関係者にも落ち着いてご覧いただける形で伝えるための静的サイトです。

従来ページとは分離した新しい会社概要サイトとして作成しています。HTMLとCSSのみで構成し、外部フォント、JavaScript、ビルド工程は使用していません。

## 公開予定URL

https://japan-product-retail.github.io/jpr-company-profile/

## ファイル構成

```text
.
├── index.html
├── styles.css
├── robots.txt
├── sitemap.xml
└── README.md
```

## GitHub Pagesでの公開手順

1. GitHubで `japan-product-retail/jpr-company-profile` というPublicリポジトリを作成します。
2. このディレクトリで、作成したリポジトリをリモートとして登録します。

   ```bash
   git remote add origin https://github.com/japan-product-retail/jpr-company-profile.git
   ```

3. 基準ブランチと作業ブランチをGitHubへ送信します。

   ```bash
   git push -u origin main
   git push -u origin codex/create-company-profile-site
   ```

4. GitHub上で次の内容のPull Requestを作成し、内容確認後に `main` へマージします。

   - Base: `main`
   - Compare: `codex/create-company-profile-site`
   - Title: `Create company profile website for Japanese art and prints`

5. リポジトリの `Settings` → `Pages` を開きます。
6. `Build and deployment` のSourceを `Deploy from a branch` にします。
7. Branchに `main`、Folderに `/(root)` を選び、保存します。
8. 数分後、公開予定URLへアクセスして表示を確認します。

## 公開前に差し替える項目

以下は公開前に必ず確認してください。

| 項目 | 現在の表示 | 確認箇所 |
|---|---|---|
| 古物商許可番号 | `第971052200606号` | `index.html` の会社概要 |
| メールアドレス | `contact@japan-product-retail.com` | meta以外の連絡先、JSON-LD |
| 電話番号 | `090-9784-7764` | 会社概要、連絡先、JSON-LD |
| 所在地の詳細表記 | `沖縄県中頭郡北谷町` | 本文、会社概要、JSON-LD |
| canonical URL | GitHub Pages予定URL | `index.html` の `link rel="canonical"` |
| OGP URL | GitHub Pages予定URL | `index.html` の `og:url` |
| Organization URL | GitHub Pages予定URL | `index.html` のJSON-LD |
| sitemap URL | GitHub Pages予定URL | `sitemap.xml` と `robots.txt` |

電話番号とメールアドレスは既存公開ページから確認した内容を反映しています。所在地の番地以降と古物商許可番号は、運用者が最終確認した情報へ差し替えてください。

## 独自ドメインへ変更する場合

たとえば `https://japan-product-retail.com/` を使用する場合は、次の箇所を同じURLへ揃えます。

1. `index.html`
   - canonical
   - `og:url`
   - JSON-LDの `url`
2. `sitemap.xml`
   - `<loc>` のURL
3. `robots.txt`
   - `Sitemap:` のURL
4. リポジトリのルート
   - `CNAME` ファイルを追加し、使用するドメインのみを1行で記載
5. GitHub Pages設定
   - `Custom domain` に使用するドメインを登録
   - DNS設定後にHTTPSを有効化

URL変更後は、ブラウザでcanonical、OGP、サイトマップが新しいURLを参照していることを確認してください。

## Google Search Consoleで行うこと

1. 公開URLまたは独自ドメインのプロパティを追加します。
2. `URL検査` でトップページを確認します。
3. `インデックス登録をリクエスト` を実行します。
4. `サイトマップ` から `sitemap.xml` を送信します。
5. 数日後、ページのインデックス状況と構造化データの認識状況を確認します。

## 更新時の確認

- `index.html` 内の会社情報とJSON-LDの内容が一致していること
- `robots.txt` と `sitemap.xml` が公開URLを参照していること
- メールリンクと電話リンクが正しく動作すること
- PCとスマートフォンの両方で表やナビゲーションが読みやすいこと
- 見出し階層が `h1` → `h2` → `h3` の順になっていること

ローカルで確認する場合は、このディレクトリで次のコマンドを実行し、表示されたURLを開きます。

```bash
python3 -m http.server 8000
```
