# Dash

例1:
```html
<svg xmlns="http://www.w3.org/2000/svg" width="120" height="120">
  <rect width="100" height="100" x="10" y="10" fill="white" id="rect">
  </rect>
  <line x1="5" y1="5" x2="190" y2="5" stroke="#000" id="line"/>
</svg>
```

```css
svg {}

#rect {
  stroke: red;
  stroke-width: 1px;
  stroke-dasharray: 400;
  stroke-dashoffset: 400;
  animation: dash 1s linear;
  animation-fill-mode: forwards;
}

#line {
  stroke: red;
  stroke-width: 1px;
  stroke-dasharray: 200;
  stroke-dashoffset: 200;
  animation: dash 1s linear;
  animation-fill-mode: forwards;
  animation-delay: .5s;
}

@keyframes dash {
  to {
    stroke-dashoffset: 0;
  }
}
```

## 外周の計算方法 
```js
let points = [[273,0],[0,224],[152,586],[634,520],[702,160], [273,0]];
let res = calcAll(points)
console.log(`total: ${~~res}`);

function calcAll(points) {
  let [total, last] = [0, undefined];
  points.map(
    (p) => {
      let current = { x: p[0], y: p[1] };
      if (last) total += calc( last, current);
      last = current;
    }
  );
  return total;
}

function calc(p1, p2) {
  let width = Math.abs(p1.x - p2.x);
  let height = Math.abs(p1.y - p2.y);
  return pytha(width, height);
}

function pytha(a, b) {
  return Math.sqrt(a * a + b * b);
}
```
