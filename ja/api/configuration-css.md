---
title: 'API: css プロパティ'
description: Nuxt.js ではグローバルに適用したい（すべてのページにインクルードしたい）CSS ファイル/モジュール/ライブラリを設定できます。
---

# css プロパティ

> Nuxt.js ではグローバルに適用したい（すべてのページにインクルードしたい）CSS ファイル/モジュール/ライブラリを設定できます。

`sass` を利用したい場合は `node-sass` および `sass-loader` パッケージをインストールしてください。もしインストールしていなければ:

```sh
npm install --save-dev node-sass sass-loader
```

- タイプ: `配列`
- 要素: `文字列`

`nuxt.config.js` 内で CSS リソースを追加するには:

```js
module.exports = {
  css: [
    // node モジュールを直接ロードする (ここでは SASS ファイル)
    'bulma',
    // プロジェクト内の CSS ファイル
    '@/assets/css/main.css',
    // プロジェクト内の SCSS ファイル
    '@/assets/css/main.scss'
  ]
}
```

Nuxt.js は拡張子から自動的にファイルタイプを推測して Webpack のための適切なプリプロセッサローダを使用します。ただし使用する必要のあるローダは各自でインストールしてください。
