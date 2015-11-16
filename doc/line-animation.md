# Line Animation

例) 徐々に線を描く

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
