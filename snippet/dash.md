# Dash

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
