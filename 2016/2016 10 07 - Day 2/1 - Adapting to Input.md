# Adapting to Input

:bust_in_silhouette: [Jason Grigsby](https://cloudfour.com/thinks/)  
:bird:               [@grigs](https://twitter.com/grigs)  
:tv:                 [Video](https://vimeo.com/194967832)

---

## A history lesson

- In the beginning the Web was formless
- Then 640x480 was the canvas, then 800x600, then 1024x768
- Then Mobile came
- Realization: the Web has no fixed canvas
- In the past different frameworks for desktop and Mobile
  - Why? Different platfoms with different usability considerations!

## Four truths about input

### 1: Input is exploding

- 1874: keyboard
- 1984: mouse (+ GUI), cursor devices
- 1996: scroll wheel
- 2005/2006: camera
- 2007+: multi-touch plus bunch of sensors
- 2011: Siri
- Look at the pace! Not slowing down!
- Next: Microsoft HoloLens with Gestures (video demo)
  - Remember Leap Motion?
- Next: Pre-sensing touch
  - Hover is back!

:arrow_right: The last decade has seen everything from accelerometers to GPS to 3D touch. **Input is not slowing down!**

### 2: Input is a continuum

- Phones have keyboards and cursors; desktop computers have touchscreens
- Hover, pointer events, keyboard events
- *Demo: Chromebook Pixel*
  - Larger buttons using touch vs. smaller buttons using a mouse

### 3: Input is undetectable

- Browser detection of touch‚ and nearly every other input type, is unreliable
- You just cannot make assumptions on input based on screen size/form factor
  - Like hover on desktop vs. mobile
  - Like typing on desktop vs. mobile
- Bad solution: detecting touch! (can be enabled by default on Chrome desktop)
- Bad solution: detecting mouse or keyboard!
- Save us from ourselves

### 4: Input is transient

- Knowing what input someone uses one moment tells you little about what will be used next
- Input = Schrödinger’s Cat
  - You can detect it when it’s used
  - Input can be added or removed in seconds, so you cannot rely on certain input method

## Input considerations

### 1: Design for the largest target by default

- Fitt’s Law
  - Use larger controls
  - Touch: recommended size 10mm
  - Keyboard/mouse: recommended size 7mm

:arrow_right: Design touch first (largest target use)

### 2: Design for modes of interation instead of input

- Consider display density
  - Larger rows in Gmail
  - Couch Mode in Vimeo

:arrow_right: Design for user need, not for input

### 3: Make things accessible

- D-pad controls (Nintendo controls, Apple Remote)
  - Support arrow key events
  - Feature undetectable, thus support arrow key navigation by default

:arrow_right: Support accessibility features

### 4: Design for multiple concurrent inputs

- Mouse + keyboard
- Touch + trackpad (see Chromebook Pixel)

:arrow_right: Combine inputs for great UX

### 5: Abstract baseline input

- Wording: Tap, click :arrow_right: point, select
- Incompatibilities: 2 sets of events (mouse, touch)
- Pointer Events to the rescue!
  - Shipped in Edge, FF/Chrome in development
  - pep.js polyfill

:arrow_right: Use Pointer Events

### 6: Progressively enhance input

- Use Geolocation
  - But what about other sensors like compass, gyroscope? Try to use it!
- Use Camera
  - Scan credit card on iOS, works but you should test it
    - Use AutoFill and new Payment Request API / Apple Pay o.t. Web
    - Consider testing AutoFill (QA)
  - Camera stream (i.e. for Photobooth)
- Use speech recognition
  - Works in Chrome and somehow in Firefox
- Use the physical Web using Bluetooth
  - Beacons

### 7: Make input part of test plans

- Add inputs to your device labs (like Styluses)
  - Open Device Lab ftw!

:arrow_right: See article on ALA for more info: [Adapting to Input](http://alistapart.com/article/adapting-to-input)

## Learn from mobile context mistakes

- People want to do the same things like on desktop
- We think real keyboards are better, but many people are faster on virtual keyboards
- Who are we to judge? **We need to learn to adapt!**
