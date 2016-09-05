# SVGTransform

## Method
- `initialize()` - SVGPoint を初期化
- `getItem()` - 
- `insertItemBefore()` - 
- `replaceItem()` - 
- `removeItem()` - 
- `appendItem()` -
- `createSVGTransformFromMatrix()` - 
- `consolidate()` - 


### Sample (SVGPoint)

```js
const NS = 'http://www.w3.org/2000/svg';
let svg = document.createElementNS(NS, 'svg');
let pt = svg.createSVGPoint();

let polyline = document.createElementNS(NS, 'polyline');

// get item in points attribute
polyline.points.getItem(0);

// replace item
let pt2 = svg.createSVGPoint();
pt2.x = 20;
pt2.y = 20;
polyline.points.replaceItem(pt2, 2);

// remove item
polyline.points.removeItem(3);

// append item
let pt3 = svg.createSVGPoint();
pt3.x = 100;
pt3.y = 100;
polyline.points.appendItem(pt3);

// Points attribute is initalized.
polyline.points.initialize(pt);
```
