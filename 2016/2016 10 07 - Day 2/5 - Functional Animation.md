# Functional Animation

🗣 [Sarah Drasner](http://sarahdrasnerdesign.com/)  
[@sarah_edo](https://twitter.com/sarah_edo)

## Let's start from the beginning

- websites start looking all the same
- CTA buttons are powerful
- growth-hacking
- user-testing

=> Animation gets a bad rap.

**Invisible animation vs. immersive animation**

## Invisible animation

= UX animation, UX choreography

- don't interrupt users
- reduce cognitive leaks
- give users an idea of sense of place
- do not use modals on Mobile, breaks content (*brute force* UX)
- motion solves user problems
- good animation = good branding
- a11y: disable animation via toggle!
- Demo time: Barcelona site, maps…
- animation supports user flow
- animation needs to be added at start, not as sugar on top
- spatial awareness (like seat selection and actual movie view)
- space conservation

### performance

- opacity & transform really performant
- hardware acceleration ftw. (translateZ)
- use Chrome devtools for debugging animations (to prevent jank)

## immersive animation

- DOM/virtual DOM
  - great for UI/UX animation
  - great for SVG (resolution independent)
  - easier to debug
  - tanks with a lot of object
  - you must take care about the way you animate
- canvas
  - dance pixels dance
  - great for really impressive 3d animation
  - movvement of tons of object
  - hard to make accessible
  - not res independent out of the box
  - breaks to nothing
- SVG animation
  - very good support
  - crisp on any display
  - less HTTP requests
  - easily scalable for responsive
  - small filesize if designed for perf
  - easy to animate (has a DOM)
  - easy to make accessible
  - interactive and immersive
  - narrative
  - also good for prototyping
- Responsive SVG
  - media queries to reduce complexity and stuff for smaller screens
- GreenSock (GSAP)
  - cool animation API
  - solves cross-browser incosistencies
  - support for timelines
    - stack tweens
	- add telative labels
	- animate scenes
  - Demo: Greensock timeline
- Animation can be responsive
- SVG (incl. animation) can be accessible
- combine SVG animation with audio, good for narration, very performant
- CSS-Tricks logo has animation easter egg on hypen
- try to work with storyboards so you have a plan of your animations
- Demo: Hipster Elephant Game
  - React
  - SVG
  - GreenSock
- Demo: Growing Balloon (audio + SVG animation)
- Demo: Smoke Animation in SVG
- Demo: Candle Animation in SVG

> The Web has so much potential - even old techs like SVG
