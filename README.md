# SVG (Scalable Vector Graphics)
SVG の学習や情報収集のまとめ

## 基本構文

```xml
<svg version="1.1" xmlns="http://www.w3.org/2000/svg" 
  width="[width]" height="[height]" viewBox="[x] [y] [width] [height]">
  <defs>
    <linearGradient id="Gradient1" x1="0" x2="0" y1="0" y2="1">
      <stop offset="0%" stop-color="red"/>
      <stop offset="50%" stop-color="black" stop-opacity="0"/>
      <stop offset="100%" stop-color="blue"/>
    </linearGradient>

    <radialGradient id="Gradient2" cx=".5" cy=".5" r=".5" fx=".25" fy=".25" spreadMethod="repeat" gradientUnits="">
      <stop offset="0%" stop-color="red"/>
      <stop offset="100%" stop-color="blue"/>
    </radialGradient>

    <pattern id="Pattern" x="5" y="5" width="50" height="50" patternUnits="userSpaceOnUse" patternContentUnits="userSpaceOnUse">
      <rect x="0" y="0" width="50" height="50" fill="skyblue"/>
      <rect x="0" y="0" width="25" height="25" fill="url(#Gradient1)"/>
      <circle cx="25" cy="25" r="20" fill="url(#Gradient2)" fill-opacity=".5"/>
    </pattern>
    
    <clipPath id="Clip">
      <rect x="0" y="0" width="200" height="100"/>
    </clipPath>
    
    <mask id="Mask">
      <rect x="0" y="0" width="200" height="200" fill="url(#Gradient1)"/>
    </mask>
  </defs>

  <rect x="[length]" y="[length]" width="[size]" height="[size]"/>
  <rect x="[length]" y="[length]" width="[size]" height="[size]" rx="[length]" ry="[length]"/>
  <circle cx="[length]" cy="[length]" r="[length]"/>
  <ellipse cx="[length]" cy="[length]" rx="[length]" ry="[length]"/>
  <line x1="[length]" y1="[length]" x2="[length]" y2="[length]"/>
  <polyline points="[x1],[y1] [x2],[y2] [x3],[y3] ..."/>
  <polygon points="[x1],[y1] [x2],[y2] [x3],[y3] ..."/>
  <path d="[command1 x1 y1] [command2 x2 y2] ..."/>
  <text x="[length]" y="[length]" font-size="[size]" text-anchor="[keyword]" fill="[color]">
    Hello World
    <tspan x="[x]" dx="[dx]" rotate="[deg]" textLength="[length]">Hello</tspan> World
    <tref xlink:href="[Path]"/>
    <textPath xlink:href="[Path]">Hello world</textPath>
  </text>
  <image x="10" y="10" width="100" height="100" xlink:href="path/to/image">

  <!-- 例) Call "#Gradient1" -->
  <rect x="10" y="10" rx="15" ry="15" width="100" height="100" fill="url(#Gradient1)"/>
  <!-- 例) Call "#Gradient2" -->
  <rect x="10" y="120" rx="15" ry="15" width="100" height="100" fill="url(#Gradient2)"/>
  <!-- 例) Call "#Pattern" -->
  <rect x="120" y="10" width="200" height="200" fill="url(#Pattern)" stroke="black"/>
  <!-- 例) Text path -->
  <text></text>
  <!-- 例) Clipping -->
  <circle cx="100" cy="100" r="100" clip-path="url(#Clip)"/>
  <!-- 例) Masking -->
  <rect x="10" y="10" width="100" height="100" mask="url(#Mask)"/>


  <g transform="translate(30, 40) rotate(45)">
  </g>
</svg>
```

## プロパティ

```css
/**
 * @prop {fill} [color] - 塗りつぶしの色
 * @prop {fill-rule} [nonzero | evenodd | inherit] - 図形の内側の領域を定義する
 * @prop {fill-opacity} [opacity] - 塗りつぶしの透明度
 * @prop {stroke} [color] - アウトラインの色
 * @prop {stroke-with} [size] - 線の太さ
 * @prop {stroke-opacity} [opacity] - 線の透明度
 * @prop {stroke-linecap} [butt | round | square] - 線の端のスタイル
 * @prop {stroke-linejoin} [miter | round | bevel] - 線の頂点の下いる
 * @prop {stroke-dasharray} [numbers] - 点線や破線のパターン
 * @prop {stroke-dashoffset} [number] - 点線の始まりの位置
 */
```

## Tools
- [SVG Path Builder](http://anthonydugois.com/svg-path-builder/) - SVGのパスを生成する
- [SVG Icons - Ready to use SVG Icons for the web.](http://svgicons.sparkk.fr/) - SVG アイコン

## References
- [SVG | MDN](https://developer.mozilla.org/ja/docs/Web/SVG)
- [SVGコードの基本 | CodeGrid](https://app.codegrid.net/entry/svg-basic)
- [SVG 1.1 仕様 （第２版） 日本語訳](http://www.hcn.zaq.ne.jp/___/SVG11-2nd/index.html)
- [スタイル付け – SVG 1.1 （第２版）](http://www.hcn.zaq.ne.jp/___/SVG11-2nd/styling.html)
- [svg要素の基本的な使い方まとめ](http://www.h2.dion.ne.jp/~defghi/svgMemo/svgMemo.htm)
- [SVG Primer](http://www.w3.org/Graphics/SVG/IG/resources/svgprimer.html)
- [How to Design, Code, and Animate SVGs](http://surbhioberoi.com/a-complete-guide-to-svg/)
- [SVGアニメーションの現状(2015/7/10)](http://postd.cc/the-state-of-svg-animation/)
- [Practical SVG](http://alistapart.com/article/practical-svg) - viewBox など
