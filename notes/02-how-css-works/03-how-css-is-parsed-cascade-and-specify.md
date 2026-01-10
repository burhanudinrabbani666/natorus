# CASCADE AND SPECIFY

## Cascade

Process of combining diffenrent stylesheets and resolving conflicts between different CSS rules and declarations, when more than one rule applies to a certain element.

## IMPORTANCE (WEIGHT) ==> SPECIFICITY ==> SOURCE ORDER

### IMPORTANCE

1. User !importance declarations
2. Author !importance declarations
3. Author declarations
4. User declarations
5. Default browser

### SPECIFICITY

1. Inline Styles
2. IDs
3. Classes, pseudo-classes, attribute
4. Elemenets, psuedo-elements

### SOURCE ORDER

The last decalrattion in the code wwill override all other decalrations and will be applied

## WHAT YOU NEED TO KNOW

- CSS declarations with !importance have the highest priority
- But, only use !importance as the last resource, its beetter to use correct specificities - **more maintainable code**
- inline style will always have priority over styles in external stylesheets
- A selector that contacins 1 id is more specific than one with 1000 classes
- A selector that contacins 1 class is more specific than one with 1000 elements
- The universal selector \* has no specificitiy calue(0,0,0,0)
- Rely more on specificity than on the order of selectors
- But, rely on order whhn using 3rd party stylesheets --> always put your author stylesheets last

[Next: Specificity in practice](./04-specify-in-practice.md)
