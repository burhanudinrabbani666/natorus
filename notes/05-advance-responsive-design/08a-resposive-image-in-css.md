# RESPONSIVE IMAGE IN CSS

```css
@media (min-resolution: 192dpi) and (min-width: 900px), (min-width: 2000px) {
  background-image:
    linear-gradient(
      to right bottom,
      rgba(variables.$color-secondary-light, 0.8),
      rgba(variables.$color-secondary-dark, 0.8)
    ),
    url("/img/hero.jpg");
}
```

[Next: Testing](./09-testing.md)
