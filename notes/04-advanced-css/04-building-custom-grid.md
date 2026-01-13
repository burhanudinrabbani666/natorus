# BUILDING CUSTOM GRID

We create a grid for layout. The grid class is ready to use depending on your needs.

- [Grid scss file](/sass/layouts/_grid.scss)

Example:

```scss
.col-1-of-2 {
  width: calc((100% - #{variables.$gutter-horizontal}) / 2);
}

.col-1-of-3 {
  width: calc((100% - 2 *#{variables.$gutter-horizontal}) / 3);
}
```

[Next: Building about section](./05-building-about-section.md)
