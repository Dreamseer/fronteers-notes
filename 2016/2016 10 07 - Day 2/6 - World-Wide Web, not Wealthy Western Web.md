# World-Wide Web, not Wealthy Western Web

🗣 [Bruce Lawson](http://www.brucelawson.co.uk/)  
[@brucel](https://twitter.com/brucel)

---

## You should make the Web better for …

- Developers
- Consumers
- Business owners
- The next 4 billion people

**Ask yourself: Where will your next customers come from?**

- Asia has 4 billion people at the moment
  - China: 1.3 bn. people, 7.7% GDP growth
  - Myanmar: 13.6% GDP growth
  - India: 190 million online users now, 400 million next year
- What do these nations have in common?
  - See themselves as global citizens
  - People come online on smartphones, Mobile-only
- Top domains:
  - USA: Google, Facebook, YouTube, Wikipedia (on high-end handsets)
  - Indonesia: Facebook, Google, WordPress (on low-end handsets)

## Make the Web work on lower-spec devices

- Embrace PWA
  - “Install” apps on home screen
  - Icon
  - Full screen, portrait, landscape
  - App lives on the Web
  - Native apps take up space (460 MB vs. 1 MB for typical apps)
    - Installation fails due to flaky networks
  - Use a manifest JSON
  - [pwa.rocks](https://pwa.rocks/)
  - Requires no app store
  - Lives on the server, no update required
  - Works offline
- Service Workers 🎉
  - Enables push notifications (but don’t spam, yo!)
  - Enables background sync (useful for flaky networks)
- Responsive images
  - Makes site faster
  - Saves up to 70% of bandwidth
- Networks Notworks
  - Solution: proxy browsers (Opera Mini, Chrome, Opera Turbo and stuff)
  - **Opera Mini**
    - Works with Thor (server on Iceland), minimizes site to about 10%
    - New ad-blocking: sites in general are 14% faster, Facebook is even 35% faster
    - 89% less data, 14% less battery
- Battery life matters 🔋 (think of your daily commute)

## Design considerations for the developing worlds

- Color! (i.e. don’t use red in Thailand: means death)
- Don’t use given + family name fields, just use a single name field
- JS-only APIs don’t work on proxy browsers
- Proxy browsers don’t support CSS features which drain battery (animation, gradients, web fonts)
- Icons: Use SVG instead of fonts
- Serve HTML instead of JS that serves HTML (ask Airbnb, it’s faster, who knew?)

‼️ Whoa. 😳 Watch video later for more details on Asian and African development of Internet usage, lots of stats and stuff.
