# Offline, Progressive and Multithreaded: A peek at the web apps of the future

@nolanlawson => Slides linked on Twitter

- PWA = latest buzzword
- service worker + app manifest + push notifications + IndexedDB
- Flash, Silverlight < HTML5
- Desktop: HTML won, Mobile: Native (atm)
- PWAs win over Native due to “Progressive”
- Offline
  - pouchDB, localForage are great IndexedDB wrappers
  - Offline-first
    - not really about actual offline state
	- it's about speeeeeeeed
	- latency latency latency
	- memory is faster than disk is faster than network
	- autocompletion enhanced with local storage
    - old vs. new:
	  - Static data: App Cache vs. Cache API (SW)
	  - Dynamic query data: Local Storage and WebSQL vs. IndexedDB
	    - Local Storage has race conditions and is synchronous => BOO!
		- IndexedDB is asynchronous and transaction-based, but hard to work with (use an abstraction, dude!)
- Progressive
  - websites progressively become apps
  - weak version: progressively add features
  - strong version: must work w/o JS (see Adactio's famous post)
    - many people don't get their sites to work w/o JS (i.e. Facebook, Gmail, Trello)
  - smartphones have JS support, but connectivity may be weak, thus use JS and keep offline in mind
  - do not use a big JS file to rule them all => super slow
    - critical HTML/CSS first, user sees stuff
	- then download JS
	- server-side React, Fastboot, Angular 2 isolated renderer ftw.
	- pokedex.org works with 2G and offline, super-fast critical rendering
- Multithreaded
  - Why? Because *jank* (see classic NES games)
  - Web Workers, run JS in a different thread
  - experiment: better frame rates with React + Web Workers
  - a lot of dev complexity, thus less used in real apps
 - It’s all about *the user*. Better UX!

## QA

- missed it, look up other notes :-(
