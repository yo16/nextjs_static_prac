# nextjs_static_prac
next.jsで静的サイトを作成するサンプル

# 環境構築
## アプリの初期設定
```
npx create-next-app@latest
```

## `output: 'export'`を追加する
```TypeScript:app/next.config.mjs
/** @type {import('next').NextConfig} */
const nextConfig = {
    output: 'export'
};

export default nextConfig;
```


# 開発
## ビルド
```
npm run build
```
- outフォルダに静的ファイルが生成される。
- 静的ファイルは`/`から始まるパスになるため、ローカルで実行すると、`C:/favicon.ico`などにアクセスして、file not foundとなる。

## 試行
```
npx serve out
```


# 参考
- [Deploying: Static Exports | Next.js](https://nextjs.org/docs/app/building-your-application/deploying/static-exports)
- [Next.jsで静的なサイトを作ってみよう｜Next.jsとStripeではじめるシンプルなECサイト開発ワークショップ](https://zenn.dev/stripe/books/stripe-nextjs-use-shopping-cart/viewer/step1-1_nextjs_ssg)


