# WHAT IS SASS AND HOW DOES IT WORK?

## SASS

Sass is CSS prepoccessor, an extension of CSS that adds power and elegance to the basic language.

**Variables**: for reusable values such a colors, font-sizes, spacing, etc.
**Nesting**: to nest inside of one another, allowing us to write code.
**Operators**: for mathematical operations right inside of CSS.
**Partials** and import to write CSS in different files and importing them all into one single file.
**Mixins** to write reusable pieces of CSS code.
**Functions** similiar to mixins, with the difference that they produce a value that can than be used.
**Extends** to make seleector inherit declarations that are common to all of them.
**Control** directives for writting complex code using conditionals and loops.

#### SASS Syntax

```sass
.navigation
  list-style: none
  float: left

  & li
    display: inline-block
    margin-left: 30px
```

#### SCSS Syntax

```scss
.navigation {
  list-style: none
  float: left

  & li{
    display: inline-block
    margin-left: 30px
  }
}
```

[Next: Varibale and nesting](./02-variable-and-nesting.md)
