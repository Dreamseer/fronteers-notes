# Functional Animation

:bust_in_silhouette: [Sarah Drasner](http://sarahdrasnerdesign.com/)  
:bird:               [@sarah_edo](https://twitter.com/sarah_edo)  
:tv:                 [Video](https://vimeo.com/194963386)

---

## Let’s start from the beginning

- Websites start looking all the same
- CTA buttons are powerful
- Growth-hacking
- User-testing

:arrow_right: But animation gets a bad rap :disappointed:

Learn about **invisible animation vs. immersive animation**

## Invisible animation

*= UX animation, UX choreography*

- Don’t interrupt users
- Reduce cognitive leaks
- Give users an idea of sense of place
- Do not use modals on Mobile, breaks content (*brute force* UX)
- Motion solves user problems
- Good animation = good branding
- Accessibility tip: Disable animation via toggle!
- *Demo time: Barcelona site, maps…*
- Animation supports user flow
- Animation needs to be added at start, not as sugar on top:
  > "If animation just feels like the sugar on top, that’s because you treated it that way."
- Think of spatial awareness (like seat selection and actual movie view)
  - See [Smoothstate.js](https://github.com/miguel-perez/smoothState.js)
- Space conservation

### Performance

- `opacity` and `transform` are really performant
- Hardware acceleration ftw. (`translateZ`)
- Use Chrome devtools for debugging animations (to prevent jank)

## Immersive animation

**Animation using the DOM/virtual DOM:**

- :white_check_mark: Great for UI/UX animation
- :white_check_mark: Great for SVG (resolution independent)
- :white_check_mark: Easier to debug
- :no_entry_sign: Tanks with a lot of objects
- :no_entry_sign: You must take care about the way you animate

**Animation using canvas:**

- :white_check_mark: Dance, pixels, dance!
- :white_check_mark: Great for really impressive 3D animation or immersive stuff
- :white_check_mark: Movement of tons of objects
- :no_entry_sign: Harder to make accessible
- :no_entry_sign: Not resolution independent **out of the box**
- :no_entry_sign: Breaks to nothing

**Use SVG for your animations:**

- Very good browser support
- Crisp on any display
- Less HTTP requests
- Easily scalable for responsive
- Small filesize if designed for performance
- Easy to animate (has a DOM after all)
- Easy to make accessible
- Interactive and immersive
- Narrative
- Also good for prototyping
- Responsive SVG
  - Media queries to reduce complexity and stuff for smaller screens

### Meet [GreenSock](http://greensock.com/) (GSAP)

- Cool animation API
- Solves cross-browser incosistencies
- Support for timelines
  - Stack tweens
  - Add relative labels
  - Animate
  - …
  - *Demo: Greensock timeline*

## Some takeaways

- Animation can be responsive
- SVG (incl. animation) can be accessible
- Combine SVG animation with audio, good for narration, very performant
- [CSS-Tricks](https://css-tricks.com) logo has animation easter egg on hyphen
  - Try to work with storyboards so you have a plan of your animations
- *Demo: Hipster Elephant Game*
  - React
  - SVG
  - GreenSock
- *Demo: Growing Balloon* (audio + SVG animation)
- *Demo: Smoke Animation in SVG*
- *Demo: Candle Animation in SVG*

> The Web has so much potential – even old techs like SVG
