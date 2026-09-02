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

## Cloudflare Workers

Git 連携時は、Cloudflare Workers Builds で次の値を指定します。

- Build command: `pnpm build`
- Deploy command: `pnpm exec wrangler deploy`
- Node.js version: `22.13.0` 以上

静的ファイルの出力先 `dist` は `wrangler.toml` の `[assets]` で指定しています。Wrangler でローカル確認する場合は `pnpm cf:dev`、公開する場合は Cloudflare にログイン後 `pnpm deploy` を実行します。
