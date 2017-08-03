# The Best Way to Create Fantastic 'Invisible Pen' Effects in SVG
- [Site point](https://www.sitepoint.com/how-to-create-the-invisible-pen-effect-in-svg-using-vivus-js/)

## Exploring Vivus
```html
<script src="path/to/vivus.js"></script>
```

```html
<svg id="canvas">
  <path.../>
  <path.../>
  <path.../>
</svg>

<script>
new Vivus('canvas', { duration: 300 }, callback)
</script>
```

## The Five Drawiing  Options of Vivus

```js
new Vuvus('canvas', {
  start: 'autostart',
  type: 'delayed',
  duration: 200,
})
```
## One-By-One

```js
new Vivus('canvas', {
  start: 'autostart',
  type: 'oneByOne',
  duration: 300,
})
```

## Async

```js
mew Vivus('canvas', {
  start: 'autostart',
  type: 'async',
  duration: 300,
})
```

## scenario

```js
mew Vivus('canvas', {
  start: 'autostart',
  type: 'scenerio',
})
```

```html
<line data-start="200" data-duration="200" .../>
<line data-start="0" data-duration="100" .../>
<line data-star="100" data-duration="10" .../>
```

## Scenario-Sync
- `data-duration`
- `data-delay`
- `data-async`

```js
new Vivus('canvas', {
  start: 'autostart',,
  type: 'scenario-sync',
})
```

```html
<line .../>
<line data-delay="100" .../>
<line data-duration="300" data-async .../>
<line data-duration="200" .../>
```

## Complete Examples
### Car Bluprint Drawing

```js
new Vivus('canvas', {
  start: 'autostart',
  type: 'delayed',
  animTimingFunction: Vivus.EASE,
}, function(car) {
  setTimeout(function() {
    car.reset().play()
  }, 3000)
})
```


## Rocket Drawing

```js
new Vivus('canvas', {
  start: 'autostart',
  type: 'scenario-sync',
  pathTimingFunction: Vivus.EASE_OUT,
}, function(obj) {
  obj.el.classList.add('fill-1', 'fill-2', 'fill-3', 'fill-4', ..., 'clear-stroke')
})
```

```html
<path data-duration="50" .../>
<path data-duration="150" data-delay="100" .../>
<path data-duration="50" .../>
<path data-duration="50" .../>
<g>
  <polygon data-duration="300" data-async .../>
</g>
<path data-delay="300" .../>
<path .../>
<g>
  <polygon data-async .../>
  <polygon data-async .../>
</g>
```
