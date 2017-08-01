# Managing SVG plugins

- [Snap.svg](http://snapsvg.io/)
  - [Snap.svgの使い方まとめ](http://www.h2.dion.ne.jp/~defghi/snapsvg/snapsvg.xhtml)
  - [Snap.svgで快適SVGアニメーション](https://app.codegrid.net/entry/snapsvg-1)
- [Vivus](https://github.com/maxwellito/vivus)<br>
  - `type: senario-sync` ではDOMの記述の順番にアニメーションする
  - `data-async` 属性を与えると非同期にアニメーションする
  - コールバック関数を渡すとエラーが出る

```js
Uncaught Error: Vivus [constructor]: "callback" parameter must be a function
    at Vivus.setCallback (vivus.js:503)
    at new Vivus (vivus.js:329)
    at (index):54
Vivus.setCallback @ vivus.js:503
Vivus @ vivus.js:329
(anonymous) @ (index):54
```
