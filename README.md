# SVG

SVG の学習や情報収集のまとめ

__基本構文__

```xml
<svg version="1.1" xmlns="http://www.w3.org/2000/svg" 
  width="[width]" height="[height]" viewBox="[x] [y] [width] [height]">
  <defs>
    <linearGradient id="Gradient1" x1="0" x2="0" y1="0" y2="1">
      <stop offset="0%" stop-color="red"/>
      <stop offset="50%" stop-color="black" stop-opacity="0"/>
      <stop offset="100%" stop-color="blue"/>
    </linearGradient>
    <radialGradient id="Gradient2" cx=".5" cy=".5" r=".5" fx=".25" fy=".25">
      <stop offset="0%" stop-color="red"/>
      <stop offset="100%" stop-color="blue"/>
    </radialGradient>
  </defs>

  <rect x="[length]" y="[length]" width="[size]" height="[size]"/>
  <rect x="[length]" y="[length]" width="[size]" height="[size]" rx="[length]" ry="[length]"/>
  <circle cx="[length]" cy="[length]" r="[length]"/>
  <ellipse cx="[length]" cy="[length]" rx="[length]" ry="[length]"/>
  <line x1="[length]" y1="[length]" x2="[length]" y2="[length]"/>
  <polyline points="[x1],[y1] [x2],[y2] [x3],[y3] ..."/>
  <polygon points="[x1],[y1] [x2],[y2] [x3],[y3] ..."/>
  <path d="[command1 x1 y1] [command2 x2 y2] ..."/>
  <text x="[length]" y="[length]" font-size="[length]" text-anchor="[keyword]" fill="[color]">Text</text>

  <!-- 例) id:Gradient1 を呼び出す -->
  <rect x="10" y="10" rx="15" ry="15" width="100" height="100" fill="url(#Gradient1)"/>
  <!-- 例) id:Gradient2 を呼び出す -->
  <rect x="10" y="120" rx="15" ry="15" width="100" height="100" fill="url(#Gradient2)"/>
  <g>
  </g>
</svg>
```

__プロパティ__

```css
/*
 * @prop {fill} [color] - 塗りつぶしの色
 * @prop {stroke} [color] - アウトラインの色
 * @prop {stroke-with} [size] - 線の太さ
 * @prop {stroke-opacity} [opacity] - 透明度
 * @prop {stroke-linecap} [butt | round | square] - 線の端のスタイル
 * @prop {stroke-linejoin} [miter | round | bevel] - 線の頂点の下いる
 * @prop {stroke-dasharray} [numbers] - 点線や破線のパターン
 * @prop {stroke-dashoffset} [number] - 点線の始まりの位置
 */
```

## パス

|コマンド|説明|パラメータ|
|:--|:--|:--|
|`M` `m`| Move to |`M [x] [y]`|
|`L` `l`| Line to |`L [x] [y]`|
|`H` `h`| Horizontal line |`H [x]`|
|`V` `v`| Vertical line |`V [y]`|
|`Z` `z`| Close path |`Z`|
|`C` `c`| Cubic bezier curve |`C [x1] [y1], [x2] [y2], [x] [y]`|
|`S` `s`| Cubic bezier curve |`S [x2] [y2] [x] [y]`|
|`Q` `q`| Quadratic bezier curve |`Q [x1] [y1], [x] [y]`|
|`T` `t`| Quadratic bezier curve |`T [x] [y]`|
|`A` `a`| Arc |`A [rx] [ry] [x-axis-rotation] [large-arc-flag] [sweep-flag] [x] [y]`|


## ツール

- [SVG Path Builder](http://anthonydugois.com/svg-path-builder/) - SVGのパスを生成する
- [SVG Icons - Ready to use SVG Icons for the web.](http://svgicons.sparkk.fr/) - SVG アイコン


## リファレンス

- [SVG | MDN](https://developer.mozilla.org/ja/docs/Web/SVG)
- [SVGコードの基本 | CodeGrid](https://app.codegrid.net/entry/svg-basic)
- [SVG 1.1 仕様 （第２版） 日本語訳](http://www.hcn.zaq.ne.jp/___/SVG11-2nd/index.html)
- [スタイル付け – SVG 1.1 （第２版）](http://www.hcn.zaq.ne.jp/___/SVG11-2nd/styling.html)
- [svg要素の基本的な使い方まとめ](http://www.h2.dion.ne.jp/~defghi/svgMemo/svgMemo.htm)
