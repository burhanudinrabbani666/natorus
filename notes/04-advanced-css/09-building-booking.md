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

creating nice effect form input

```scss
@use "../abstracts/variables";

.form {
  &__group:not(:last-child) {
    margin-bottom: 2rem;
  }

  &__input {
    font-size: variables.$default-font-size;
    border-radius: variables.$default-border-radius-small;
    background-color: rgba(variables.$color-white, 0.5);

    padding: 1.5rem 2rem;
    border: none;
    border-bottom: 3px solid transparent;
    display: block;
    width: 90%;

    color: inherit;
    font-family: inherit;

    transition: all 0.4s;

    &:focus {
      outline: none;
      box-shadow: 0 1rem 2rem rgba(variables.$color-black, 0.1);
      border-bottom: 3px solid variables.$color-primary;
    }

    &:focus:invalid {
      border-bottom: 3px solid variables.$color-secondary-dark;
    }

    &::-webkit-input-placeholder {
      color: variables.$color-grey-dark2;
    }
  }

  &__label {
    font-size: 1.2rem;
    font-weight: 700;
    margin-left: 2rem;
    margin-top: 0.7rem;
    display: block;

    transition: all 0.3s ease;
  }

  &__input:placeholder-shown + &__label {
    opacity: 0;
    visibility: hidden;
    transform: translateY(-4.5rem);
  }
}
```
