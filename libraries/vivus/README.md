# Vivus
- [vivus.js - svg animation](https://maxwellito.github.io/vivus/)
- [Github](https://github.com/maxwellito/vivus)
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

## Using basically

```html
// Inline SVG
<svg id="my-svg"> ... </svg>

// Dynamic load
<object id="my-svg" type="image/svg-xml" data="link/to/my.svg"></object>

// Dynamic include to DOM
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
