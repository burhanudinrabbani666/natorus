# IMPLEMENT CSS TO SASS

```scss
.header {
  height: 95vh;

  background-image: linear-gradient(
      to right bottom,
      rgba($color-primary-light, 0.8),
      rgba($color-primary-dark, 0.8)
    ), url("/img/hero.jpg");
  background-size: cover;
  background-position: top;

  clip-path: polygon(0 0, 100% 0, 100% 75vh, 0 100%);
  position: relative;

  &__log-box {
    position: absolute;
    top: 4rem;
    left: 4rem;

    cursor: pointer;
  }

  &__logo {
    height: 3.5rem;
  }

  &__text-box {
    position: absolute;
    top: 40%;
    left: 50%;
    transform: translate(-50%, -50%);

    text-align: center;
  }
}
```

[Next: implement the 7-1 css architecture](./02-implement-7-1.md)
