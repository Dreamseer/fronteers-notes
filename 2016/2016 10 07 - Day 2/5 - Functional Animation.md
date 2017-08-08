# Functional Animation

🗣 [Sarah Drasner](http://sarahdrasnerdesign.com/)  
🐦 [@sarah_edo](https://twitter.com/sarah_edo)
📺 [Video](https://vimeo.com/194963386)

---

## Let’s start from the beginning

- Websites start looking all the same
- CTA buttons are powerful
- Growth-hacking
- User-testing

➡️ But animation gets a bad rap 🙁

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

- ✅ Great for UI/UX animation
- ✅ Great for SVG (resolution independent)
- ✅ Easier to debug
- 🚫 Tanks with a lot of objects
- 🚫 You must take care about the way you animate

**Animation using canvas:**

- ✅ Dance, pixels, dance!
- ✅ Great for really impressive 3D animation or immersive stuff
- ✅ Movement of tons of objects
- 🚫 Harder to make accessible
- 🚫 Not resolution independent **out of the box**
- 🚫 Breaks to nothing

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
