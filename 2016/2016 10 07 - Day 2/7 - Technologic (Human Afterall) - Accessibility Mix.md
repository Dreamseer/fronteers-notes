#  Technologic (Human Afterall): Accessibility Mix

🗣 [Léonie Watson](http://tink.uk/)  
[@leoniewatson](https://twitter.com/leoniewatson)

> Buy it, use it, break it, fix it

- HTML has roles (like “link”)
- provide accessible information
- DIV / SPAN are inert, no role, no state
- keyboard focus on several elements:
  - A
  - Button
  - Input / Textarea / Select / …
- order is important
- expected interactions using ENTER (or SPACE)
- DOM tree, but also: Accessibility tree
  - gets updated on DOM changes
- Accessibility APIs
  - integrated in OS
- ARIA
  - provides roles (dialog, toolbar, etc.)
  - provides attributes for accessible names and descriptions
  - provides 9 states (aria-checked, aria-pressed, aria-hidden, aria-invalid, aria-current and more)
- Demo: HTML buttons w/o accessibility information
  - add focus with tabindex="0"
  - add button role with role="button"
  - add state with aria-expanded="false", toggle when opened
  - add relationship between button and revealed content using aria-controls="{id}"
  - add aria-hidden for unneeded information for screenreaders, takes sth. out of a11y tree
    - better: `hidden` attribute
  - add keyboard events additionally to mouse events
- testing a11y APIs
  -  Tenon API
    - requires API key + application URL
    - allows some optional parameter
  - Ember a11y Test Suite
  - React a11y API
  - Angular is a bit harder; you need NGARIA which makes things easer
  - test yourself: unplug mouse, use keyboard on your site and fix all the things, zoom max in and try to work with your site
- 1996: Space Jam
  - website from 1996 is still up
  - oldschool techniques
  - you couldnt do anything on an a11y POV
- 2001: CSS1 came, and later CSS 2.1 with ::before/::after
  - generated content is accessibly supported
- CSS3: Flexbox
  - DOM order vs. order property => bad for a11y users
  - use order only for visual, not logical content order
    - maybe use tabindex for keyboard order matching box order
      - tabindex=0 = fits things in natural tab order
	  - tabindex=-1 = makes things focusable
	  - tabindex=>0 = no good idea
  - aria-flowto adds another navigation method, more complexity
  - Firefox “bug” to the rescue: updates keyboard sequence acc. to box order
- a11y does not have to be perfect, just a little bit better than yesterday => think about a11y
