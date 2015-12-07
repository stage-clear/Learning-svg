# Learning SVG

SVG の学習や情報収集のまとめ

__基本構文__

```xml
<svg version="1.1" xmlns="http://www.w3.org/2000/svg" width="[width]" height="[height]" viewBox="[x] [y] [width] [height]">
  <defs>
    <line x1="20" y1="100" x2="100" y2="20" stroke="black" stroke-width="2"/>
    <circle cx="60" cy="60" r="50"/>
    <ellipse cx="60" cy="60" rx="50" ry="25"/>
    <polygon points="60,20 100,40 100,80 60,100 20,80 20,40"/>
    <polyline fill="none" stroke="black" points="20,100 40,60 70,80 100,20"/>
    <rect x="10" y="10" width="100" height="100"/>
    <rect x="10" y="10" width="100" height="100" rx="15" ry="15"/>
    <path d="M 100 100 L 300 100 L 200 300 z" fill="red" stroke-width="3"/>

    <g>
    </g>
  </defs>
</svg>
```

```css
svg {
  fill: [color];                /* 塗りつぶしの色 */
  /* Outline Styles */
  stroke: [color];              /* アウトラインの色 */
  stroke-width: [size];         /* 線の太さ */
  stroke-opacity: [opacity];    /* 透明度 */
  stroke-linecap: [keyword];    /* 線の端のスタイル (butt|round|square) */
  stroke-linejoin: [keyword];   /* 線の頂点の下いる (miter|round|bevel) */
  stroke-dasharray: [numbers];  /* 点線や破線のパターン */
  stroke-dashoffset: [number];  /* 点線の始まりの位置 */
}
```

## ツール

- [SVG Path Builder](http://anthonydugois.com/svg-path-builder/) - SVGのパスを生成する
- [SVG Icons - Ready to use SVG Icons for the web.](http://svgicons.sparkk.fr/) - SVG アイコン


## リファレンス

- [SVG | MDN](https://developer.mozilla.org/ja/docs/Web/SVG)
- [SVGコードの基本 | CodeGrid](https://app.codegrid.net/entry/svg-basic)
- [SVG 1.1 仕様 （第２版） 日本語訳](http://www.hcn.zaq.ne.jp/___/SVG11-2nd/index.html)
- [スタイル付け – SVG 1.1 （第２版）](http://www.hcn.zaq.ne.jp/___/SVG11-2nd/styling.html)
- [svg要素の基本的な使い方まとめ](http://www.h2.dion.ne.jp/~defghi/svgMemo/svgMemo.htm)
