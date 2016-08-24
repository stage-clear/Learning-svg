# Dash

例1:
```html
<svg xmlns="http://www.w3.org/2000/svg" width="120" height="120">
  <rect width="100" height="100" x="10" y="10" fill="white">
  </rect>
</svg>
```

```css
svg {
}
svg > rect {
  stroke: red;
  stroke-width: 1px;
  stroke-dasharray: 400;
  stroke-dashoffet: 400;
  animation: dash 1s linear;
}

@keyframes dash {
  from {
    stroke-dashoffset: 400;
  }
  to {
    stroke-dashoffset: 0;
  }
}
```

例2:

```xml
<svg width="200" height="200" x="10" y="190">
  <line x1="10" y1="10" x2="190" y2="10"/>
</svg>
```

```css
svg line {
  stroke: #000;
  stroke-dasharray: 200;
  stroke-dashoffset: 200;
  animation: dash 1s linear forwards;
}

@keyframes dash {
  to {
    stroke-dashoffset: 0;
  }
}
```
