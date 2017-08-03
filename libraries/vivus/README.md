# Vivus
- [vivus.js - svg animation](https://maxwellito.github.io/vivus/)
- [GitHub - maxwellito/vivus](https://github.com/maxwellito/vivus)
- [vivus - cdnjs.com](https://cdnjs.com/libraries/vivus)

## Install
CDN:
```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/vivus/0.4.1/vivus.js"></script>
```

NPM:
```bash
$ npm install vivus
```

## Using simply

```html
<!-- Inline SVG -->
<svg id="my-svg"> ... </svg>

<!-- Dynamic load -->
<object id="my-svg" type="image/svg-xml" data="link/to/my.svg"></object>

<!-- Dynamic include to DOM -->
<div id="my-svg"></div>
```

```js
// Inline SVG / Dynamic load:
new Vivus('my-svg', {
  duration: 200,
})

// Dynamic include:
new Vivus('my-svg', {
  duration: 200,
  file: 'link/to/my.svg',
})
```

## Examples:
- [Basic](https://jsfiddle.net/walfo/aax6yjy3/)

## Memos:
- `type: senario-sync` では DOM の記述の順番にアニメーションする
- `data-async` 属性を与えると非同期にアニメーションする

## ERROR?
コールバック関数を渡すとエラーが出力される
```js
Uncaught Error: Vivus [constructor]: "callback" parameter must be a function
    at Vivus.setCallback (vivus.js:503)
    at new Vivus (vivus.js:329)
    at (index):54
Vivus.setCallback @ vivus.js:503
Vivus @ vivus.js:329
(anonymous) @ (index):54
```

```js
const myCallback = function() {}
console.log(myCallback instanceOf Function) // true
console.log(myCallback.constructor === Function) // false
```


## References
- [The Best Way to Create Fantastic 'Invisible Pen' Effects in SVG](https://www.sitepoint.com/how-to-create-the-invisible-pen-effect-in-svg-using-vivus-js/)
