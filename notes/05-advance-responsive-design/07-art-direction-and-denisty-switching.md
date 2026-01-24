# ART DIRECTION AND DENSITY

### DENSITY

Giving the broswer to render the best img.

```html
<img
  srcset="img/logo-green-1x.png 1x, img/logo-green-2x.png 2x"
  alt="Full logo"
  class="footer__logo"
/>
```

## ART DIRECTION

Warp the img with the picture than you can put an option for browser. this make image responsive with screen capability.

```html
<picture class="footer__logo">
  <source
    srcset="img/logo-green-small-1x.png 1x, img/logo-green-small-2x.png 2x"
    media="(max-width: 37.5em)"
  />
  <img
    srcset="img/logo-green-1x.png 1x, img/logo-green-2x.png 2x"
    alt="Full logo"
  />
</picture>
```

[Next: Denisty and resolution swithing](./08-denisty-and-resolution-swithing.md)
