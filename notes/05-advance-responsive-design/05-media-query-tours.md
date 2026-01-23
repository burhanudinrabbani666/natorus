# MEDIA QUERY TOURS

## CARD

Dont have any rotate hover animation.

```scss
@include mixins.respond(tablet-potrait) {
  // Function
  height: auto;
  border-radius: 3px;
  background-color: variables.$color-white;
  box-shadow: 0 1.5rem 4rem rgba(variables.$color-black, 0.25);

  &__side {
    height: auto;
    position: relative;

    box-shadow: none;

    &--back {
      transform: rotateY(0);
      clip-path: polygon(0 15%, 100% 0, 100% 100%, 0 100%);
    }
  }

  &:hover &__side--front {
    transform: rotateY(0);
  }

  &__details {
    padding: 1rem 3rem;
  }

  &__cta {
    width: 100%;
    position: relative;
    top: 0;
    left: 0;
    transform: translate(0);

    padding: 7rem 4rem 4rem 4rem;
  }

  &__price-box {
    margin-bottom: 3rem;
  }
  &__price-value {
    font-size: 6rem;
  }
}
```
