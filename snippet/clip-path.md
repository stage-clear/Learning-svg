# Clip path

# Clip Path

例: 円形に切り抜く

```xml
<img class="mask" src="https://cdn1.iconfinder.com/data/icons/hawcons/32/699748-icon-102-document-file-xml-512.png">

<svg xmlns="http://www.w3.org/2000/svg" width="512" height="512" viewBox="0 0 512 512">
  <clipPath id="myClip">
    <circle cx="150" cy="200" r="100" fill="#ccc"></circle>
  </clipPath>
</svg>
```

```css
.mask {
  clip-path: url(#myClip);
}
```
