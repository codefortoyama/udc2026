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
- `handson-0.md` → `/handson-0/`
- `_config.yml`（Minimal Mistakes設定、`remote_theme: mmistakes/minimal-mistakes@4.24.0`）
- `assets/eyecatch.svg`（アイキャッチ兼OGP）、`assets/favicon.svg`
- `assets/css/main.scss`（テーマ読み込み＋最小限の上書き）
- `_includes/head/custom.html`（favicon読み込み）
- `Gemfile`（ローカル確認用、Windows対応でtzinfo-data/wdm/webrick等を含む）

## アクセシビリティ
axe-coreで全3ページのcolor-contrast違反0を確認済み（`C:\Users\tomin\AppData\Local\Temp\opencode\a11y\audit.js`）。
背景画像上の見出しはaxeが自動判定できないため、実ピクセル測定（measure.js）で白文字15.71:1を確認。
