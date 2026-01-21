# THE POWER OF SASS MIXINS TO WRITE MEDIA QUERY

### Topics to learn

- How to use powefull sass mixins to write all media query
- How to use the @content and @if Sass directive
- Taking advantage of chrome DevTools for responsive design

## Use sass mixins to write media query

```scss
html {
  font-size: 62.5%; // Overall rem;  1rem = 10px; 10px/16px = 62.5%

  // form bigger to  small
  @include mixins.respond(tablet-landscape) {
    font-size: 56.5%; // 1 rem = 9px, 9px/16px = 56.5%  <== this is @content
  }

  @include mixins.respond(tablet-potrait) {
    font-size: 50%; // 1 rem = 8px, 8px/16px = 50%      <== this is @content
  }

  // This min
  @include mixins.respond(big-desktop) {
    font-size: 75%; // 1 rem = 12px, 12px/16px = 75%    <== this is @content
  }
}
```

## use the @content and @if Sass directive

```scss
@mixin respond($breakpoint) {
  @if $breakpoint == phone {
    @media (max-width: 37.5em) {
      // 600px
      @content;
    }
  }

  @if $breakpoint == tablet-potrait {
    @media (max-width: 56.25em) {
      // 900px
      @content;
    }
  }

  @if $breakpoint == tablet-landscape {
    @media (max-width: 75em) {
      // 1200px
      @content;
    }
  }

  @if $breakpoint == big-desktop {
    @media (min-width: 112.5em) {
      // 1800px
      @content;
    }
  }
}
```

[Next: Media query base](./03-media-query-base.md)
