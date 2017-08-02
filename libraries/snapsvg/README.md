# Snap.svg
- [Snap.svg](http://snapsvg.io/)
- [GitHub - codegrid/2015-snapsvg](https://github.com/adobe-webplatform/Snap.svg/)
- [snap.svg - cdnjs.com](https://cdnjs.com/libraries/snap.svg/)

## Install

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/snap.svg/0.5.1/snap.svg.js"></script>
```

## Using basically

```js
const $elem = Snap('.selector')
const $button = document.querySelector('button')
const play = () => {
  $elem.attr({ width: 128, height: 128 })
  $elem.animate({
    width: 256,
    height: 256,
  }, 1000)
}
$button.addEventListener('click', play, false)
```

## References:
- [Snap.svgの使い方まとめ](http://defghi1977.html.xdomain.jp/tech/snapsvg/snapsvg.xhtml)
- [Snap.svgで快適SVGアニメーション](https://app.codegrid.net/entry/snapsvg-1)
