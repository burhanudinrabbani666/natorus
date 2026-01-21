# BUILDING PURE CSS POPUP

### Key topics

- How to build nice popup with only css.
- How to use :target psuedo-class.
- How to create boxes with equal height using display: table-cell.
- how to create CSS text columns.
- How to auatomatically hypernate words using _hypens_.

## Display: table-cell

```scss
&__content {
  @include mixins.centering;
  background-color: variables.$color-white;
  box-shadow: 0 2rem 4rem rgba(variables.$color-black, 0.8);

  border-radius: 4px;
  width: 70%;
  transform: translate(-50%, -50%);
  display: table;

  overflow: hidden;
}

&__left {
  width: 33.333%;
  display: table-cell;
}
&__right {
  width: 66.6666%;
  display: table-cell;
  vertical-align: middle;
  padding: 3rem 5rem;
}
```

### Text Columns and hypens

```scss
&__text {
  font-size: 1.4rem;
  margin-bottom: 4rem;

  column-count: 2;
  column-gap: 4rem; // 1em = 16px
  column-rule: 1px solid variables.$color-grey-light-2;

  -moz-hyphens: auto;
  -ms-hyphens: auto;
  -webkit-hyphens: auto;

  hyphens: auto;
}
```
