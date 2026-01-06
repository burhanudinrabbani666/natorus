# Building header

## Clip path

[MDN: Clip path](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/clip-path)

The clip-path CSS property creates a clipping region that sets what part of an element should be shown. Parts that are inside the region are shown, while those outside are hidden.

## Centering Header

using position: absolute

```css
.header {
  clip-path: polygon(0 0, 100% 0, 100% 85%, 0 100%);
}

.text-box {
  position: absolute;
  top: 40%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```
