# SVGPathElement

## Usage
### Simple example
```html
<svg xmlns="http://www.w3.org/2000/svg">
  <defs>
    <path d="M10 10 H 90 V 90 H 10 L 10 10" id="path"/>
  </defs>
  
  <!-- The Use get referenct<xml:href> from path -->
  <use xml:href="#path"/>
</svg>
```

## Methods
- `getTotalLength()` - パスの長さを取得
- `getPointAtLength( float length )` - 与えた長さにおけるパス上の座標を返す
- `getPathSegAtLength( float length)` - 

## Path commands

|Command|Feature|Parameters|
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

## Links
- [SVGPathElement](https://developer.mozilla.org/ja/docs/Web/API/SVGPathElement) - MDN
- [Paths - SVG](https://developer.mozilla.org/ja/docs/Web/SVG/Tutorial/Paths) - MDN

## References and Hints
- [SVGのパスに沿ってDOMを動かす](http://qiita.com/takumifukasawa/items/b3df19bba0950d3c64be)

