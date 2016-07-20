# Document Archtecture

## `<svg>`

```xml
<svg xmlns="http://www.w3.org/2000/svg">
</svg>
```

## `<g>`
グラフィックス要素をグループ化するためのコンテナ要素  
`<desc>` と `<title>` とグループ化の併用により、文書構造と意味論の情報が与えられるようになる

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

```xml
<svg version="1.1" xmlns="http://www.w3.org/2000/svg">
  <desc>グループは入れ子にできる</desc>
  <g>
    <g>
    </g>
  </g>
</svg>
```

## `<defs>`
再利用可能な内容の定義
