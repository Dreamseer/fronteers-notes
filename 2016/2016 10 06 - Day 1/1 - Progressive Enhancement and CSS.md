# Progressive Enhancement and CSS

:bust_in_silhouette: [Ire Aderinokun](https://ireaderinokun.com/)  
:memo:               [bitsofco.de](https://bitsofco.de/)  
:bird:               [@ireaderinokun](https://twitter.com/ireaderinokun)  
:tv:                 [Video](https://vimeo.com/194815985)

---

## What is it?

### 2003: Graceful degredation

- Designer don’t test more than a version back
- Expensive to retrofit to new alternate devices
- Does not address different needs of different audiences

### Progressive Enhancement

- Web design must mature
- Must accept development of the past years
- Goal of web design is not to dazzle, but to deliver information to widest audience

## What does that mean in practice?

- Semantic markup for all content
- Correct elements in correct order
- Content in plain text, most accessible, best for PE
- Enhanced layout by CSS
  - CSS = enhancement, not requirement
- Enhanced behavior by JS
  - JS = enhancement, not requirement
- End-user prefs should be respected
  - Do not use `user-scalable=no` and stuff

## Why important today?

- Many more browsers and versions
- Many more new technologies
- Many more people online, thus more different user needs

> The Web is still open!

## Progressive Enhancement

### What can go wrong with JS?

- Maybe not enabled (like in Opera Mini)
- Browser does not support certain features
- JS should be an enhancement, key functionality should work w/o JS
- Load polyfills if needed

### What can go wrong with HTML?

- If browser does not understand a new element, it sees DIVs
- Add ARIA roles like `role="main"` for more semantics

### What about CSS?

- If browser does not support a preoperty or value, nothing happens
- No built-in fallbacks in CSS
- Start with sensible HTML
- M&Ms: Core is HTML, everything else is extra layer
- Take advantage of cascade
  - Use legacy code first
    - i.e. vendor prefixes above unprefixed version
- Go mobile first
  - `min-width` > `max-width`
  - Sth. that looks good on mobile looks a lot more usable on desktop
- Use Flexbox
  - Designed to be a Progressive Enhancement
  - Use it on your production sites
- Last resort: use different stylesheets
  - i.e. for old IE
  - Example: BBC “cutting the mustard”
- Use CSS feature queries
  - `@supports (property: value) { … }`
  - Detects all or either of several features, too
  - `@supports not (property: value) { … }` works, too
  - Support is quite good (no IE, no Opera Mini)
- Good example: `object-fit`
  - Use feature queries *and* use advantage of cascade

## 2016

- VR + watches in the game
- New technologies like Angular 23 :smile:
- More people online with different hardware

Thus:

> Leave no one behind!

## QA

- How far back should you go with support for older devices and stuff?
  - Difficult, different for everyone
  - Opera Mini used in some regions, different baseline
  - Look at your audience
- Problem: Industry overlooks Opera Mini?
  - People should be more aware of their user base and browser usage
  - If you’re lucky, use more advanced features
- PE = challenges for designers and developers, do designers have to take care of it?
  - Designers have to take it into account
- What is the biz case for PE?
  - Again it’s about user base
  - If you use PE, it’s a faster, better experience for everyone
