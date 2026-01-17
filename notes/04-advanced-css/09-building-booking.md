# BUILDING BOOK

make the background color cut without clip-path property

```scss
.book {
  background-image:
    linear-gradient(
      105deg,
      rgba(variables.$color-white, 0.9) 0%,
      rgba(variables.$color-white, 0.9) 50%,
      transparent 50%
    ),
    url(/img/nat-10.jpg);
  background-size: 100%;
  border-radius: variables.$default-border-radius-small;
  box-shadow: 0 1.25rem 4rem rgba(variables.$color-primary-dark, 0.2);

  height: 50rem;

  &__form {
    width: 50%;
    padding: 1.6rem;
  }
}
```
