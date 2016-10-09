# Building Responsive CSS Components

🗣 [Zell Liew](http://zellwk.com/)  
[@zellwk](https://twitter.com/zellwk)

## Responsive components

- We think about modularity
  - Question: not why, but how?
  - Communicate with team

## Scalability

- Nobody thinks about it
- Parent component uses `rem`, child component uses `em`
  - Scales nice
  - Proportionally sized typography/images
- How much do we need to scale?
  - Scale not to infinity (and beyond)
  - Proportional scaling upwards and downwards
- Design principle of repetition
  - Limit number of font-sizes (and repeat them)
  - Maybe we need only two button styles
  - Consistent whitespace (`line-height`, `margin`, vertical rhythm)
- *Demo: Mashable article teaser item*
- Why `rem`?
  - `em` = local var, `rem` = global var
  - We think: local = good, global = bad, but not the case in CSS
  - **Use `em` for anything that is relative to `font-size`, otherwise use `rem`**
  - Good for vertical rhythm

## Breakpoints + scaling

- Scaled full-width components may become smaller on larger screens in a grid
- Obvious solution: Nested breakpoints
  - But: Many media queries, so *things get complicated*
  - And: Duplication of styling

### Meet Element Queries

- Elements know about their size, you can style according to it
- `.comp`, `.comp[min-width: 600px]` etc.
  - Not valid CSS (yet), you need JS to polyfill
  - Polyfill: support of progressive enhancement is hard
  - Code gets still duplicated

### Valid CSS alternatives

- Use mixins to prevent code duplication
  - Style mixins for `base`, `small`, `medium`, `large`, etc.

## Summary

- Determine component area maps
- Determine breakpoints and changes in styles
- Determine units for CSS properties
- Handle complex variations with mixins or element queries
- **Don’t overengineer**
