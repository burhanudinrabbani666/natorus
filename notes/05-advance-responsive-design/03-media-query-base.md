# MEDIA QUERY BASE, TYPOGRAPHY AND LAYOUT

### typography

```scss
.heading-secondary {
  font-size: 3.5rem;
  text-transform: uppercase;
  font-weight: 700;
  display: inline-block;
  letter-spacing: 2px;

  background-image: linear-gradient(
    to right,
    variables.$color-primary-light,
    variables.$color-primary-dark
  );

  background-clip: text;
  color: transparent;

  transition: all 0.3s;

  @include mixins.respond(tablet-potrait) {
    font-size: 3rem;
  }

  @include mixins.respond(phone) {
    font-size: 2.5rem;
  }

  &:hover {
    transform: skewY(2deg) skewX(15deg) scale(1.05);
    text-shadow: 0.5rem 1rem 2rem rgba(variables.$color-black, 0.2);
  }
}
```

[Next: Media query layout](./04-media-query-layout.md)
