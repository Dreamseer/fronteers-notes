# Building Responsive CSS Components

🗣 [Zell Liew](http://zellwk.com/)  
[@zellwk](https://twitter.com/zellwk)

## resp. components

- we think about modularity
  - question: not why, but how?
  - communicate with team

# scalability

- nobody thinks about it
- parent comp: `rem`, child comp: `em`
  - scales nice
  - proportionally sized typography/images
- how much do we need to scale?
  - not to infinity (and beyond)
  - proportional scaling upwards and downwards
- design principles
  - principle of repetition
    - limit number of font-sizes (and repeat them)
	- maybe we need just two button styles
	- consistent whitespace (`line-height`, `margin`, vertical grid)
- Demo: Mashable article teaser item
- why `rem`?
  - em = local var, rem = global var
  - we think: local = good, global = bad, not in CSS
  - **site in `em` of sth. is relative to `font-size`, otherwise use `rem`**
  - good for vertical rhythm

## breakpoints + scaling

- scaled full-width components may become smaller on larger screens in a grid
- nested breakpoints
- many media queries => *things get complicated*
- duplication of styling

## Meet Element Queries

- elms know about their size, you can style acc. on it
- .comp, .comp[min-width: 600px] etc.
  - not valid CSS (yet), you need JS to polyfill
  - polyfill: support of PE is hard
  - code gets still duplicated

## Valid CSS alternatives

- use mixins to prevent code duplication
  - style mixins for base, small, medium, large, …

## Summary

- determine comp. area maps
- determine breakpoints and changes in styles
- determine units for CSS properties
- handle complex variations with mixins or element queries
- don't overengineer
