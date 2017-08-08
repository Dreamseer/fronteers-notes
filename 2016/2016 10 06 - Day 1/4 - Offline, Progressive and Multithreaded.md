# Offline, Progressive and Multithreaded: A peek at the web apps of the future

🗣 [Nolan Lawson](http://nolanlawson.com/)  
🐦 [@nolanlawson](https://twitter.com/nolanlawson) (slides linked on Twitter)
📺 [Video](https://vimeo.com/194834593)

---

## PWA = latest buzzword

- PWA = service worker + app manifest + push notifications + IndexedDB
- HTML5 > Flash, Silverlight
- Desktop: HTML won, Mobile: Native (atm.)
- PWAs win over Native due to “Progressive”

## Offline

- pouchDB, localForage are great IndexedDB wrappers
- Offline-first
  - Not really about actual offline state
  - It’s all about speeeeeeeed 🏎
    - Latency latency latency
    - Memory is faster than disk is faster than network
  - Autocompletion example enhanced with Local Storage
- Old vs. new:
  - Static data: App Cache vs. Cache API (SW)
  - Dynamic query data: Local Storage and WebSQL vs. IndexedDB
    - Local Storage has race conditions and is synchronous ➡️ BOO!
    - IndexedDB is asynchronous and transaction-based, but hard to work with (use an abstraction, dude!)

## Progressive

- Websites progressively become apps
  - Weak version: progressively add features
  - Strong version: must work w/o JS (see Adactio’s [famous post](https://adactio.com/journal/10708))
    - Many people don’t get their sites to work w/o JS (i.e. Facebook, Gmail, Trello)
- Smartphones have JS support, but connectivity may be weak, thus use JS and keep *offline* in mind
- Do not use a big JS file to rule them all ➡️ super slow
  - Critical HTML/CSS first, user sees stuff
  - Then download JS
  - Server-side React, Fastboot, Angular 2 isolated renderer FTW!
  - [pokedex.org](https://www.pokedex.org) works with 2G and offline, super-fast critical rendering

## Multithreaded

- Why? Because *jank* (see classic NES games which become slow when many things happen)
- Web Workers: run JS in a different thread
- Experimental: better frame rates with React + Web Workers
- A lot of development complexity, thus less used in real apps
- It’s all about *the user* and *better UX*!

## QA

- Missed it, look up other notes 😔
