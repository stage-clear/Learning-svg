# SVGTransform

## Method
- `initialize()` - SVGPoint を初期化


### initialize

```js
const NS = 'http://www.w3.org/2000/svg';
let svg = document.createElementNS(NS, 'svg');
let pt = svg.createSVGPoint();

let polyline = document.createElementNS(NS, 'polyline');

// Points attribute is initalized.
polyline.points.initialize(pt);

```
