[English](README.md) | 日本語


hiragino-fix.css
================

ヒラギノ角ゴシック (hiragino Sans) の表示ウエイトをブラウザ間で統一するための小さな CSS ライブラリです。具体的には Safari の挙動に合わせます。

参考文献: https://jeffreyfrancesco.org/weblog/2025022801/


インストール
------------

npm, yarn, pnpm でインストールします。以下は npm での例です。

```shell
npm install @jforg/hiragino-fix.css
```

必要であれば CSS ファイルを任意のディレクトリにコピーしてください。


使い方
------

HTML で `<link>` タグを使って読み込むか、

```html
<link href="/path/to/hiragino-fix.css" rel="stylesheet">
```

CSS で `@import` を使用します（`layer()` はオプション）。

```css
@import url(@jforg/hiragino-fix.css) layer(typeface);
```

※後者の場合、パフォーマンス上の理由から [post-css-import][psi] や [esbuild][esb] などを使ってバンドルすることをおすすめします。

あとは任意の要素（通常は `html` か `body` でしょう）に `font-family` プロパティを設定してください。

```css
html {
  font-family: Hiragino Sans, sans-serif;
}
```


License
-------

[CC0 1.0 Universal][cc0]


[pci]: https://github.com/postcss/postcss-import
[esb]: https://esbuild.github.io/
[cc0]: https://creativecommons.org/publicdomain/zero/1.0/
