# Portfolio

Astro で作る静的ポートフォリオサイトです。Cloudflare Pages への公開を前提に設定しています。

## ローカル開発

```sh
pnpm install
pnpm dev
```

## ビルド

```sh
pnpm build
```

成果物は `dist/` に生成されます。

## Cloudflare Pages

Git 連携時は、Cloudflare Pages で次の値を指定します。

- Build command: `pnpm build`
- Build output directory: `dist`
- Node.js version: `22.12.0` 以上

Wrangler でローカル確認する場合は `pnpm cf:dev`、公開する場合は Cloudflare にログイン後 `pnpm deploy` を実行します。
