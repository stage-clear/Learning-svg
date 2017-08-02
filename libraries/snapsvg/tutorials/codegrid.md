# Tutorial <sub>by codegrid</sub>
- [Snap.svgで快適SVGアニメーション](https://app.codegrid.net/series/2015-snapsvg)


__アニメーションが実行中かどうかの判定__:<br>
```js
function isMoving() {
  var anims = $circle.inAnim()
  
  if (anims.length === 0) {
    alert(false)
  } else {
    alert(true)
  }
}
```

__カスタムイージングの作成__:<br>

```js
var customEasing = (t) => {
  return t < 0.5
    ? 0.5 * (1.0 - mina.bounce(1.0 - t * 2.0))
    : 0.5 * mina.bounce(t * 2.0 - 1.0) + 0.5
}
```

__空のSVG要素の作成__:<br>

```js
// 空のSVG要素の生成
var $root = Snap() // width: 100%, height: 100%
var $root = Snap(100, 100) // width: 100px, height: 100%
var placeholder = document.getElement('placehoder')
$root.appendTo(placeholder)
```

__要素の取得のしかた__:<br>
```js
// 存在している要素の取得（1）: snap(DOM)
// <circle id="c1" ... />
var circle = document.getElementById('c1')
var $circle = Snap(circle)

// 存在している要素の取得(2): Snap(Selector string)
// <circle id="c1" ... />
var $circle = Snap('#c1')

// 要素グループ(setインスタンス)の取得: Snap(Array)
var $set = Snap([
  Snap('#c1'),
  Snap('#c2'),
  Snap('#c3'),
])

// 子要素の取得: select
// <g id="group">
//   <circle id="c1" ... />
//   <circle id="c2" ... />
//   <circle id="c3" ... />
// </g>
var $group = Snap('#group')
var $firstCircle = $group.select(':first-child')
var $secondCircle = $group.select('#c2')

// 複数の要素を取得
// <g id="group">
//   <circle class="circle" ... />
//   <circle class="circle" ... />
//   <circle class="circle" ... />
// </g>
var $group = Snap('#group')
var circleSet = $group.selectAll('.circle')
```

__Snap.parse__:<br>
```js
var svgSource = '<circle ... />'
var $placeholder = Snap('#placeholder')
var $content = Snap.parse(svgSource)
$placeholder.append($content)
```
