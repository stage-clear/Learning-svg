# Animate

__`<animateMotion>` に `<circle>` を紐付ける__

```html
<svg>
  <animateMotion 
    xlink:href="#Circle"
    dur="3s" 
    repeatCount="indefinite" 
    fill="freeze" 
    path="M 25,50 C 37.5,25 37.5,25 50,0 75,50 75,50 100,100 50,100 50,100 0,100 12.5,75 12.5,75 25,50 Z" />

  <circle id="Circle" cx="10" cy="10" r="5" fill="red"/>
</svg>
```

__`<circle>` に `<animateMotion>` を紐付ける__

```html
<svg>
  <circle cx="10" cy="10" r="5" fill="red">
    <animateMotion 
      dur="3s" 
      repeatCount="indefinite" 
      fill="freeze" 
      path="M 25,50 C 37.5,25 37.5,25 50,0 75,50 75,50 100,100 50,100 50,100 0,100 12.5,75 12.5,75 25,50 Z" />
  </circle>
</svg>
```
