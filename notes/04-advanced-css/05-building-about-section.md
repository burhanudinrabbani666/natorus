# BUILDING ABOUT SECTION

## Part 1

use the utility class to center the heading. [Utility file](/sass/base/_utility.scss)

I also use modern properties to display the exciting hover effect.

```scss
&:hover {
  transform: skewY(2deg) skewX(15deg) scale(1.1);
  text-shadow: 0.5rem 1rem 2rem rgba(variables.$color-black, 0.2);
}
```

## Part 2

creating button

```scss
// /sass/components.scss

.btn-text {
  &:link,
  &:visited {
    color: variables.$color-primary;
    font-size: variables.$default-font-size;
    border-bottom: 1px solid variables.$color-primary;

    display: inline-block;
    text-decoration: none;
    padding: 3px;

    transition: all 0.4s;
  }

  &:hover {
    background-color: variables.$color-primary;
    color: variables.$color-white;
    box-shadow: 0 1rem 2rem rgba(variables.$color-black, 0.2);
    transform: translateY(-2px);
  }

  &:active {
    box-shadow: 0 0.5rem 1rem rgba(variables.$color-black, 0.2);
    transform: translateY(0);
  }
}
```

## Part 3

flying image

```scss
.composition {
  position: relative;

  &__photo {
    box-shadow: 0 1.5rem 4rem rgba(variables.$color-black, 0.4);

    width: 55%;
    position: absolute;
    z-index: 10;

    transition: all 0.3s;
    outline-offset: 1rem;

    &--p1 {
      left: 0;
      top: -2rem;
    }

    &--p2 {
      right: 0;
      top: 2rem;
    }

    &--p3 {
      left: 20%;
      top: 10rem;
    }

    &:hover {
      outline: 1 rem solid variables.$color-primary;
      transform: scale(1.05) translateY(-1rem);
      box-shadow: 0 2.5rem 4rem rgba(variables.$color-black, 0.5);

      z-index: 20;
    }
  }

  &:hover &__photo:not(:hover) {
    transform: scale(0.9);
    filter: blur(1px);
  }
}
```

[Next: building About section](./05-building-about-section.md)
