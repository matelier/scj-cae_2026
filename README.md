# チラシ（Marp ソース）

公開シンポジウム「計算科学と産業を結ぶAI時代の人材循環型エコシステムのあり方」

## 構成
- `poster.md` … 本体（A4縦・2ページ：表面＝告知／裏面＝次第）
- `theme/poster.css` … カスタムテーマ（`/* @theme poster */`）
- `bg_main.png` / `bg_sub.png` … 背景画像（生成画像）
- `.marprc.yml` … `html: true`, `allowLocalFiles: true`, `themeSet: theme`

## ビルド
```bash
npx @marp-team/marp-cli poster.md --pdf -o poster.pdf
npx @marp-team/marp-cli poster.md --images png --image-scale 2
```
Chromium が見つからない場合は `CHROME_PATH` を指定してください。

## 差し替えポイント
- 申込QRコード：`poster.md` の `<div class="qr">` を `<img src="qr.png">` に置換
- 配色：`theme/poster.css` の `:root` の `--navy` / `--cyan` / `--gold`
