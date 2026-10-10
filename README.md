# toyama-lp — LP (GitHub Pages + Minimal Mistakes)

公開先: https://codefortoyama.github.io/udc2026/
リポジトリ: https://github.com/codefortoyama/udc2026 （main直下がJekyllサイト、Pagesはlegacyビルド）

## ローカル確認（Windows）
Ruby 3.1を使用（3.3はJekyll 3.9と非互換のため不可）。
```powershell
$env:Path = "C:\Ruby31-x64\bin;$env:Path"
$env:PAGES_REPO_NWO = "codefortoyama/udc2026"
bundle install
bundle exec jekyll serve --livereload
# http://127.0.0.1:4000/
```

## 構成
- `index.md`（splashレイアウトのLP本体）
- `connpass.md` → `/connpass/`
- `handson-0.md` → `/handson-0/`、`mentor-0.md` → `/mentor-0/`
- `_config.yml`（Minimal Mistakes設定、`remote_theme: mmistakes/minimal-mistakes@4.24.0`）
- `assets/hero.svg`（ヒーロー背景）、`assets/eyecatch.svg`（OGP兼アイキャッチ）、`assets/favicon.svg`
- `assets/css/main.scss`（テーマ読み込み＋モダンな見た目・レイアウト・配色の上書き）
- `_includes/head/custom.html`（favicon・タスクリストのチェックボックスに読み上げラベル付与）
- `Gemfile`（ローカル確認用、Windows対応でtzinfo-data/wdm/webrick等を含む）

## アクセシビリティ・検証
- axe-core（WCAG 2.0/2.1 A・AA）で全4ページ違反0を確認。
- モバイル390px／デスクトップ1280pxで横スクロール（はみ出し）なしを確認。
- 検証はPuppeteer（Chrome）で実施。手元での再現手順は調査スクリプト群を参照。
