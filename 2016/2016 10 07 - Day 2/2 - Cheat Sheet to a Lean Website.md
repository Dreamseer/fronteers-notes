# Cheat Sheet to a Lean Website

🗣 [Barbara Bermes](http://www.bbinto.me/)  
🐦 [@bbinto](https://twitter.com/bbinto)
📺 [Video](https://vimeo.com/194962379)

---

## Why care about performance?

- People do not want to wait
- Sites are getting fatter
- 79% online shoppers won’t return to a website due to poor performance
- One second delay = 7% loss CVR ➡️ wpostats.com

## Shape performance culture

- Make everybody aware and care of performance, everybody’s business
- Feel encouraged to say “no” to things slowing down your site
- Celebrate success 🎉
  - Etsy: announces performance heroes every month on their blog
- Be transparent
  - Etsy: publishes Site Performance Reports

## Performance = perception + respect

- Perception is subjective

## How long does it take for users to interact with a page?

- Treat speed as a feature
- Optimize from user’s perspective, not with your company’s fast internet connection
- Start wireframing for performance
  - Performance point system
  - Use [WebPagetest](https://www.webpagetest.org/) for insights (film strip of loading)
  - Measurable performance modules (MPM)
    - low impact = 1 point
    - medium impact = 2 point
    - high impact = 6 point
    - load important stuff first, use performance point system

### Measure first, then optimize

- Set a performance budget
- Check competitors
- Speed index (avg. time at which visisble parts are displayed)
- PageSpeed score (by Google)
- [Speedcurve](https://speedcurve.com/) (by Steve Souders)

## The browser

- Learn about the render workflow (HTML, CSS, blocking JS, render tree, layout, paint)
- Determine critical rendering path
- Know how the browser renders (order matters)
- Keep HTML as clean as possible
- Clean up your DOM by removing unused elements
- Don’t put 3rd party features (like scripts and web fonts) in your critical path
- 14 kB rule, serve most important content first
  - 14 kB in first TCP roundtrip
  - Keep most important styles inline
- Script best practices
  - Use `defer` and `async`
  - Put script in the bottom

## Reduce bytes

- Minify HTML, CSS, JS
- Compress images
- Avoid web fonts (or consider a web font loader)
- Use Gzip techniques

## Reduce HTTP requests

- Concatenate
- Use libraries only when needed
- Create sprites
- Use data URIs

❓ *What about HTTP/2?*

## Latency

- High latency on mobile
- Reduce requests
- Reduce polling
- Send important styles in first 14 kB
- Remove reirs
- Use offline storage techniques
- Use considerations
- Use HTTP/2

## Make friends with the server

- Gzip all your assets
- Cache stuff appropriately

## Tame mobile

- Don’t make the user pay for bad performance
- Reduce requests and DNS lookups
- Remember batteries
- Consider offline
- Test on real devices

## Automate performance routines

- Task runners (Grunt, Gulp, Maven, Ant…)
  - Include performance APIs in CI

## Avoid yo-yo-effect

- Constant measuring and monitoring
- Automation incedibly helpful by triggering appropriate warnings

> Browsing should be as simple and fast as turning a page in a mag. (Larry Page)

https://twitter.com/jaronbarends/status/784308180041871361
