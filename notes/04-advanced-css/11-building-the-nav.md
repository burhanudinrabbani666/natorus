# BUILDING NAVIGATION

Here we use the checkbox property to add logic to display and remove navigation.

```html
<div class="navigation">
  <input type="checkbox" class="navigation__checkbox" id="navi-toggle" />
  <label for="navi-toggle" class="navigation__button">
    <span class="navigation__icon"></span>
  </label>
  <div class="navigation__background">&nbsp;</div>

  <nav class="navigation__nav">
    <ul class="navigation__list">
      <li class="navigation__item">
        <a href="#" class="navigation__link"><span>01</span>About Natours</a>
      </li>
      <li class="navigation__item">
        <a href="#" class="navigation__link"><span>02</span>Your benefits</a>
      </li>
      <li class="navigation__item">
        <a href="#" class="navigation__link"><span>03</span>Popular Tours</a>
      </li>
      <li class="navigation__item">
        <a href="#" class="navigation__link"><span>04</span>Stories</a>
      </li>
      <li class="navigation__item">
        <a href="#" class="navigation__link"><span>05</span>Book now</a>
      </li>
    </ul>
  </nav>
</div>
```

```scss
@use "../abstracts/variables";
@use "../abstracts/mixins";

.navigation {
  &__checkbox {
    display: none;
  }
  &__button {
    background-color: variables.$color-white;
    height: 7rem;
    width: 7rem;

    position: fixed;
    top: 6.4rem;
    right: 6.3rem;
    border-radius: 50%;
    z-index: 2000;
    text-align: center;
    cursor: pointer;

    box-shadow: 0 1rem 3rem rgba(variables.$color-black, 0.1);
  }
  &__background {
    height: 6rem;
    width: 6rem;
    border-radius: 50%;

    position: fixed;
    top: 6.5rem;
    right: 6.5rem;
    background-image: radial-gradient(
      variables.$color-primary-light,
      variables.$color-primary-dark
    );

    z-index: 1000;
    transition: transform 0.5s cubic-bezier(0.83, 0, 0.17, 1);
  }
  &__nav {
    height: 100vh;
    // width: 100%;

    position: fixed;
    top: 0;
    left: 0;
    z-index: 1500;

    opacity: 0; // initial opacity 0 => 100%
    width: 0; // initial width 0 => 100%
    transition: all 0.5s cubic-bezier(0.83, 0, 0.17, 1);
  }
  &__list {
    @include mixins.centering;

    list-style: none;
    text-align: center;
    width: 100%;
  }
  &__item {
    margin-bottom: 1rem;
  }
  &__link {
    &:link,
    &:visited {
      display: inline-block;
      font-weight: 300;
      font-size: 3rem;
      color: variables.$color-white;
      text-decoration: none;
      text-transform: uppercase;

      padding: 1rem 2rem;

      background-image: linear-gradient(
        120deg,
        transparent 0%,
        transparent 50%,
        variables.$color-white 50%
      );
      background-size: 225%;

      transition: 0.4s;

      span {
        margin-right: 1.5rem;
      }
    }

    &:hover,
    &:active {
      background-position: 100%;
      color: variables.$color-primary;

      transform: translateX(1rem);
    }
  }

  // Functionality
  &__checkbox:checked ~ &__background {
    transform: scale(80);
  }

  &__checkbox:checked ~ &__nav {
    opacity: 1;
    width: 100%;
  }

  // Icon
  &__icon {
    position: relative;
    margin-top: 3.35rem;
    &,
    &::before,
    &::after {
      width: 3rem;
      height: 2px;
      background-color: variables.$color-grey-dark3;
      display: inline-block;
    }

    &::before,
    &::after {
      content: "";
      position: absolute;
      left: 0;

      transition: all 0.2s;
    }
    &::before {
      top: -0.8rem;
    }

    &::after {
      top: 0.8rem;
    }
  }

  &__button:hover &__icon::before {
    top: -1rem;
  }

  &__button:hover &__icon::after {
    top: 1rem;
  }

  &__checkbox:checked + &__button &__icon {
    background-color: transparent;
  }

  &__checkbox:checked + &__button &__icon::before {
    top: 0;
    transform: rotate(135deg);
  }

  &__checkbox:checked + &__button &__icon::after {
    top: 0;
    transform: rotate(-135deg);
  }
}
```

[Next: Bulding pure css popup](./12-builing-pure-css-popup.md)
