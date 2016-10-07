# Adapting to Input

🗣 [Jason Grigsby](http://blog.cloudfour.com/)  
[@grigs](https://twitter.com/grigs)

- In the beginning the Web was formless
- 640x480 was the canvas, then 800x600, then 1024x768
- Then Mobile came
- Realization: the Web has no fixed canvas
- In the past different frameworks for desktop and Mobile
  - Why? diff. platfoms with diff. usability considerations
## for truths about input
### incompl. history
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
- => input is not slowing down
## input is a continuum
- hover, pointer events, keyboard
- tablets, laptops, convertibles, 23" touch screens
- you can not make assumptions on input based on screen size/form factor
  - like hover on desktop vs. mobile
  - like typing on desktop vs. mobile
  - bad solution: detecting touch! (can be enabled by default on Chrome desktop)
  - bad solution: detecting mouse or keyboard!
  - saves us from ourselvers
- Demo: Chromebook Pixel
  - larger buttons using touch vs. small buttons using a mouse
- Input = Schrödinger's Cat
  - you can detect it when it’s used
  - input can be added or removed in seconds, you cannot rely on certain input method
- Fitt’s Law
  - larger controls
  - touch: recommended size 10mm
  - keyboard: recommended size 7mm
- => design touch first (largest target use)
- display density
  - larger rows in Gmail
  - couch mode in Vimeo
  - => design for user need, not for input
- D-pad controls (Nintendo controls, Apple Remote)
  - support arrow key events
  - undetectable, thus support arrow key nav
- accessibility
## 4: design for multiple concurrent input
- mouse + keyboard
- touch + trackpad (see Chromebook Pixel)
- combine inputs for great UX
## 5: abstract input
- tap, click => point, select
- incompatbilities: 2 sets of events (mouse, touch)
- Pointer Events to the rescue
  - Edge shipped, FF/Chrome in dev
  - pep.js polyfill
## 6: progressively enhance input
- Use Geolocation
  - But what abozt compass, gyroscope?
- Use Camera
  - iOS: Scan credit card, works but you should test it
    - Use AutoFill and new Payment Request API / Apple Pay o.t. Web
    - Consider testing AutoFill (QA)
  - Camera stream (i.e. for Photobooth)
- Use speech recognition
  - Works in Chrome and somehow in FF
- Use the physical Web using Bluetooth
  - Beacons
## Make input part of test plans
- add inputs to yout device labs
  - like Styluses
  - Open Device Lab ftw!

=> @TODO see photo for summary  
=> see article on ALA by Jason

## Learn from mobile context mistakes
- people want to do the same things like on desktop
- we think real keyboards are better, but many people are faster on virtual keybpards
- who are we to judge? we need to learn to adapt
