English | [日本語](README.ja.md)


hiragino-fix.css
================

This is a tiny CSS library that normalizes the display weight of Hiragino Sans across browsers. Specifically, it matches Safari’s behavior.


Install
-------

Install via npm, yarn or pnpm. Here's an example for npm:

```shell
npm install @jforg/hiragino-fix.css
```

If necessary, copy the CSS file to a directory of your choice.


Usage
-----

Load CSS using a `<link>` tag in your HTML:

```html
<link href="path/to/hiragino-fix.css" rel="stylesheet">
```

Or use `@import` in your CSS (`layer()` is optional):

```css
@import url(@jforg/hiragino-fix.css) layer(typeface);
```

NOTE: In this case, it is recommended to bundle using a CSS processing tool (like [post-css-import][pci] or [esbuild][esb]) for performance reasons.

Then set the `font-family` property on any elemet (usually `html` or `body`).

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
