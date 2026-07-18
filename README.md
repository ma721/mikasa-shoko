# 三笠商行 物販LP

Cloudflare Pages で公開している物販ランディングページ。

## ファイル構成

```
├── index.html          公開ページ（安全版）
└── assets/labels/
    ├── label-nyusankin.jpg   乳酸菌ラベル
    ├── label-zendama.jpg     善玉菌ラベル
    └── label-kougousei.jpg   光合成細菌ラベル
```

## Cloudflare Pages 設定

- ビルドコマンド: **なし**（空欄）
- 出力ディレクトリ: **/** （ルート）
- フレームワークプリセット: **None**

静的HTMLのみなのでビルド不要。push すると自動でデプロイされる。

## よく編集する場所

`index.html` 内をエディタで検索すると見つかる。

| 直したいもの | 検索する文字列 |
|---|---|
| 購入・お問い合わせボタンの飛び先 | `href="#"` |
| 商品カードの説明文 | `card-desc` |
| 使いどころの箇条書き | `ben-card` |
| 希釈のめやす | `use-card` |
| 基本のブレンド比率 | `blend-item` |

### 商品を追加するとき

`index.html` の `<article class="card">` ブロックを1つコピーして、

1. `--accent` の色を変える
2. `<img src="...">` を新しいラベル画像に
3. 商品名・英字名・説明文・タグを差し替え

の3点を直せば増やせる。ラベル画像は `assets/labels/` に追加すること。

## メモ

- 画像はHTMLに埋め込まず外部ファイルにしている（差分を小さく保つため）
- フォントは Google Fonts から読み込み（Shippori Mincho B1 / Zen Kaku Gothic New / Cormorant Garamond）
- 表現について: 公開しているのは薬機法・景表法に配慮した安全版。別途「期待できる」表現版が手元にあるが、リポジトリには含めていない（公開されないようにするため）。
