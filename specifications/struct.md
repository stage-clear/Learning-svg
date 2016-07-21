# Document Archtecture

## [#](https://triple-underscore.github.io/SVG11/struct.html#SVGElement) `<svg>` - コンテナ要素

```xml
<svg version="1.1" xmlns="http://www.w3.org/2000/svg">
</svg>
```

## [#](https://triple-underscore.github.io/SVG11/struct.html#GElement) `<g>` - コンテナ要素
グラフィックス要素をグループ化するためのコンテナ要素  
`<desc>` と `<title>` とグループ化の併用により、文書構造と意味論の情報が与えられるようになる

__例1)__
```xml
<svg xmlns="http://www.w3.org/2000/svg" width="5cm" height="5cm">
  <desc>それぞれ2個の矩形からなる2つのグループ</desc>
  <g id="g1" fill="red">
    <rect x="1cm" y="1cm" width="1cm" height="1cm"/>
    <rect x="3cm" y="1cm" width="1cm" height="1cm"/>
  </g>
  <g id="g2" fill="blue">
    <rect x="1cm" y="3cm" width="1cm" height="1cm"/>
    <rect x="3cm" y="3cm" width="1cm" height="1cm"/>
  </g>

  <!-- rect 要素でキャンバスの境界を表示-->
  <rect x=".01cm" y=".01cm" width="4.98cm" height="4.98cm"
    fill="none" stroke="blue" stroke-width=".02em"/>
</svg>
```

__例2)__
```xml
<svg version="1.1" xmlns="http://www.w3.org/2000/svg">
  <desc>グループは入れ子にできる</desc>
  <g>
    <g>
    </g>
  </g>
</svg>
```

## [#](https://triple-underscore.github.io/SVG11/struct.html#DefsElement) `<defs>` - コンテナ要素
再利用可能な内容の定義をします

__例1)__

```xml
<svg xmlns="http://www.w3.org/2000/svg" version="1.1" width="8cm" height="3cm">
  <desc>先祖要素の defs 子要素内における局所 URI 参照</desc>
  <defs>
    <linearGradient id="Gradient01">
      <stop offset="20%" stop-color="#39f"/>
      <stop offset="90%" stop-color="#f3f"/>
    </linearGradient>
  </defs>

  <rect x="1cm" y="1cm" width="6cm" height="1cm" fill="url(#Gradient01)"/>

  <!-- rect 要素でキャンバスの境界を表示 -->  
  <rect x=".01cm" y=".01cm" width="7.98cm" height="2.98cm"
    fill="none" stroke="blue" stroke-width=".02cm"/>
</svg>
```

## [#](https://triple-underscore.github.io/SVG11/struct.html#DescriptionAndTitleElements) `<desc>` `<title>` - 記述的要素
コンテナ要素やグラフィック要素には、個別に `<desc>` またはテキストのみの説明を与える `<title>` をあるいは両方を指定することができる

__例1)__
```xml
<svg xmlns="http://www.w3.org/2000/svg" version="1.1" width="4in" height="3in">
  <g>
    <title>地域別売上高</title>
    <desc>
      これは地域別売上高を表す棒グラフである
    </desc>
    <!-- ベクターデータで定義される棒グラフ -->
  </g>
</svg>
```

__例2)__

```xml
<svg xmlns="http://www.w3.org/2000/svg" version="1.1" width="4in" height="3in">
  <desc xmlns:mydoc="http://example.org/mydoc">
    <mydoc:title>これは例示用 SVG ファイル</mydoc:title>
  </desc>
</svg>
```

## [#](https://triple-underscore.github.io/SVG11/struct.html#SymbolElement) `<symbol>` - コンテナ要素
`<symbol>` は、グラフィックのひな型オブジェクトを定義し、 `<use>` によりインスタンス化される

- `<symbol>` はそれ自身として描画されない
- `<symbol>` は、それを参照する `<use>` で定義されるビューポーと矩型に適宜 拡縮させてはめ込むための、`viewbox` 属性と `preserveAspectRatio` 属性を持つ

`<marker>`,  `<pattern>` は `<symbol>`と密接に関連する

__例)__

```xml
<svg version="1.1" xmlns="http://www.w3.org/2000/svg">
  <symbol id="a" viewBox="0 0 100 100" preserveAspectRatio="none">
    <rect width="100" height="100" x="0" y="0"/>
  </symbol>

  <use xlink:href="#a"/>
</svg>
```

## [#](https://triple-underscore.github.io/SVG11/struct.html#UseElement) `<use>` - グラフィック要素
`<use>` は、文書の与えられた場所において他の要素を参照し、そのグラフィック内容の取り込みと描画を指する  
`<image>` とは異なり、`<use>` は、文書全体を参照することはできない

`<use>` が参照し複製された（ように振る舞う）要素は非公開なので `<use>` の子として現れることはない

__例) use要素が参照した要素は子要素として存在しない__

```xml
<svg version="1.1" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <circle id="a" x="100" y="0" width="100" height="100"/>
    <rect id="b" x="0" y="0" width="100" height="100"/>
  </defs>
  
  <use x="10" y="10" xlink:href="#b"/>
</svg>
```

```css
rect {
  stroke: blue;
  stroke-width: 12px;
}

/* use 参照後も適用されます */
#b {
  stroke: green;
}

/* !! use 参照後のセレクターは適用されません */
/*    (参照元のセレクターに依存します) */
rect:first-child {
  stroke-width: 1px;
}

/* !! これは効かない */
use rect {
  stroke: yellow;
  stroke-width: 6px;
}
```

## [#](https://triple-underscore.github.io/SVG11/struct.html#ImageElement) `<image>` - グラフィック要素

## References 
- [5. 文書構造](https://triple-underscore.github.io/SVG11/struct.html)
