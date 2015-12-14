# SVG

SVG の学習や情報収集のまとめ

__基本構文__

```xml
<svg version="1.1" xmlns="http://www.w3.org/2000/svg" 
  width="[width]" height="[height]" viewBox="[x] [y] [width] [height]">
  <defs>
    <rect x="10" y="10" width="100" height="100"/>
    <rect x="10" y="10" width="100" height="100" rx="15" ry="15"/>
    <circle cx="60" cy="60" r="50"/>
    <ellipse cx="60" cy="60" rx="50" ry="25"/>
    <line x1="20" y1="100" x2="100" y2="20" stroke="black" stroke-width="2"/>
    <polyline points="20,100 40,60 70,80 100,20"/>
    <polygon points="60,20 100,40 100,80 60,100 20,80 20,40"/>
    <path d="M 100 100 L 300 100 L 200 300 z" fill="red" stroke-width="3"/>
    <text x="[number]" y="[number]" font-size="[number]" text-anchor="[keyword]" fill="[color]">Text</text>

    <g>
    </g>
  </defs>
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
