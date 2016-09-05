# appendItem to points attribute

```js
const NS = 'http://www.w3.org/2000/svg';
let svg = document.createElementNS(NS, 'svg');
let polyline = document.createElementNS(NS, 'polyline');

['0,0', '24,180', '250,189', '266,15', '0,0'].forEach((str) => {
  let pt = svg.createSVGPoint();
  let point = str.split(',');
  pt.x = point[0];
  pt.y = point[1];
  polyline.points.appendItem(pt);
});

svg.appendChild(polyline);
document.body.appendChild(svg);
```
