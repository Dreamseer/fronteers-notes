#  Technologic (Human Afterall): Accessibility Mix

:bust_in_silhouette: [Léonie Watson](https://tink.uk/)  
:bird:               [@leoniewatson](https://twitter.com/leoniewatson)  
:tv:                 [Video](https://vimeo.com/194964027)

---

> Buy it, use it, break it, fix it

## HTML and ARIA

- HTML has roles (like “link”)
  - They provide accessible information
  - `DIV` and `SPAN` are inert: no role, no state
- HTML supports keyboard usage
  - Focus on several elements:
    - `A`
    - `BUTTON`
    - `INPUT` / `TEXTAREA` / `SELECT` / …
  - Order is important
  - Expected interactions using ENTER (or SPACE)
- There is a DOM tree, but also an accessibility tree
  - Gets updated on DOM changes
- Accessibility APIs integrated in OS
- ARIA
  - Provides roles (`dialog`, `toolbar`, etc.)
  - Provides attributes for accessible names and descriptions
  - Provides 9 states (`aria-checked`, `aria-pressed`, `aria-hidden`, `aria-invalid`, `aria-current` and more)

## Use HTML + ARIA for enhanced accessibility

*Demo: HTML buttons w/o accessibility information*

- Add focus with `tabindex="0"`
- Add button role with role="button"`
- Add state with `aria-expanded="false"`, toggle when opened
- Add relationship between button and revealed content using `aria-controls="{id}"`
- Add `aria-hidden` for unneeded information for screenreaders, takes sth. out of a11y tree
  - Even better: `hidden` attribute
- Add keyboard events additionally to mouse events

## Testing a11y APIs

- Tenon API
  - requires API key + application URL
  - allows some optional parameter
- Ember a11y Test Suite
- React a11y API
- Angular is a bit harder; you need NGARIA which makes things easer

:wheelchair: Test yourself:

- Unplug mouse
- Use keyboard on your site
- Shut off screen
- Zoom max in and try to work with your site

## a11y history

- 1996: “Space Jam”
  - Website from 1996 is [still up](http://www2.warnerbros.com/spacejam/movie/jam.htm)
  - Oldschool layout techniques
  - You couldn’t do anything from an a11y POV
- 2001: CSS1 came, and later CSS 2.1 with `::before`/`::after`
  - Generated content is accessibly supported
- CSS3: Flexbox
  - DOM order vs. `order` property ➡️ bad for a11y users
  - Use `order` only for visual, not logical content order
    - Maybe use `tabindex` for keyboard order matching box order
      - `tabindex=0` = fits things in natural tab order
      - `tabindex=-1` = makes things focusable
      - `tabindex=1..n` = no good idea
  - `aria-flowto` adds another navigation method, more complexity
  - Firefox “bug” to the rescue: updates keyboard sequence acc. to box order

> Accessibility does not have to be perfect, just a little bit better than yesterday.

➡️ **Think about a11y!**
