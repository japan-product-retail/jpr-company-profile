# JPプロダクトリテイリング合同会社 公式会社サイト

沖縄を拠点とするJPプロダクトリテイリング合同会社の公式会社サイトです。日本美術・古書・版画等の取扱分野、委託販売や作品整理に関するご相談、会社概要、お問い合わせ先を掲載しています。

## 公式サイト

[JPプロダクトリテイリング合同会社](https://japan-product-retail.github.io/jpr-company-profile/)

## 構成

HTMLとCSSで構成する静的サイトです。外部フォント、実行用JavaScript、ビルド工程は使用していません。

| ファイル | 内容 |
|---|---|
| `index.html` | 会社紹介、取扱分野、会社概要、連絡先、SEOメタ情報、Organization構造化データ |
| `company/index.html` | 英語の会社概要、事業開始・法人化の歩み、事業内容、社内ツール開発 |
| `security/index.html` | Security & Infrastructure、責任者、担当範囲、セキュリティ連絡先 |
| `styles.css` | レスポンシブ表示、キーボードフォーカス、印刷用スタイル |
| `sitemap.xml` | 公式ページのサイトマップ |
| `robots.txt` | クロール設定とサイトマップURLの記述 |
| `google75e87b349fbc0edb.html` | Googleのサイト所有権確認ファイル |

GitHub Pagesのproject siteでは、このリポジトリ内の `robots.txt` はサブディレクトリに配置されます。Googleのクロール制御にはホスト直下の `robots.txt` が参照されます。

## ローカルでの表示

リポジトリのルートで以下を実行し、[ローカルプレビュー](http://localhost:8000/)を開きます。

```bash
python3 -m http.server 8000 --bind 127.0.0.1
```
