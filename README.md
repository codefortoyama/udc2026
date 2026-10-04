# toyama-lp — LP (GitHub Pages + Minimal Mistakes)

Jekyll + Minimal Mistakes（remote_theme）に移行済み。旧静的HTMLは `index-legacy.html` / `style-legacy.css` に退避。

## 公開方法（GitHub Pages）
1. この `toyama-lp/` の中身をリポジトリのルート（または `docs/`）に配置
2. Settings > Pages > Source を「Deploy from a branch」または「GitHub Actions (Jekyll)」に設定
3. `_config.yml` の `url` / `baseurl` を公開先に合わせて編集
   - 例： `url: "https://codefortoyama.github.io"`, `baseurl: "/toyama-lp"`
4. テーマは `remote_theme: mmistakes/minimal-mistakes@4.24.0` で自動取得（追加インストール不要）

## ローカル確認
```sh
bundle install
bundle exec jekyll serve
```
簡易確認だけなら `python -m http.server` でもよいが、テーマ適用状態はJekyllでの確認が必要。

## 構成
- `index.md`（splashレイアウトのLP本体）
- `connpass.md` → `/connpass/`
- `handson-0.md` → `/handson-0/`
- `_config.yml`（Minimal Mistakes設定）
- `assets/eyecatch.svg`（アイキャッチ兼OGP）、`assets/favicon.svg`
- `assets/css/main.scss`（テーマ読み込み＋最小限の上書き）
- `Gemfile`（ローカル確認用）
