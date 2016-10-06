# How you do what you do is who you are

By [Scott Olson](https://paper.fiftythree.com/scott)  
[@gscottolson](https://twitter.com/gscottolson)

## Using React to improve UX

- Paper has multiple services: phone/tablet/web app
- Transitioned from Backbone to React
- Stack:
  - Node.js
  - Express
  - Webpack
  - Babel
  - Coffescript ➡️ ES6 ➡️ Typescript
  - Stylus + Nib + inline styles in components (test-wise)
  - CSS Modules
- **React all the things**: ~450 kB bundled code

### Image preloading

- Baseline JPG or 404 image = no great UX 🙅
- Use React for loading image, broken image, final image using JS Image API
- Transparent spacer images (WHAT?) for loading and better UX ➡️ no jank
- Use data URI for spacers = no add. request
- Different aspect ratios = different spacers ➡️ embrace SVG in React
- Load images in defined orders, specifically important for Mobile

### Fluid text inputs

- i.e. for search inputs
- This works in apps, so what about the web?
  - must resize dynamically
  - must allow text selection (and other UX defaults)
  - must use placeholders
  - must work with touch and mouse
  - must behave consistent (single line, text scroll behavior)
- What about `contentEditable`?
  - allows linebreaks, allows pasted content with formatting = BOO!
- `INPUT` vs. `SPAN`
  - combine these (like I did with `SELECT`/`OUTPUT` for weg.de, yay!)
  - `placeholder` in masks with high `z-index` which catches clicks and stuff

## Form

- Enhance existing elements
- Use of floating labels (nice, but I like my solution more, https://jsbin.com/sesaco)

## Random stuff, quite fast run-through

- Different image sources
  - Redux store, graph store
  - Handling S3 errors

@TODO: Either re-watch this part or re-use other people’s notes. 😔

## QA

- Use HTTP/2 for requesting images?
  - Target is a MVP
  - Those optimizations are realistically hard to prioritize in product roadmap
  - Features > optimizations in roadmap
- React: any usage benefits?
  - Easier maintaining
  - Easier data flow support, better to test
  - Does not solve problems specifically, but quicker
