# Document Archtecture

## `<svg>`

```xml
<svg xmlns="http://www.w3.org/2000/svg">
</svg>
```

## `<g>`
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

## `<defs>`
再利用可能な内容の定義

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

## `<desc>` `<title>`
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


## References 
- [5. 文書構造](https://triple-underscore.github.io/SVG11/struct.html)
