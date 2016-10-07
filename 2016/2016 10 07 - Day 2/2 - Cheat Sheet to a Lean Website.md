# Cheat Sheet to a Lean Website

🗣 [Barbara Bermes](http://www.bbinto.me/)  
[@bbinto](https://twitter.com/bbinto)

## why care about performance?

- people do not want to wait
- sites are getting fatter
- 79% online shoppers wont return to website due to poor performance
- one sec delay = 7% loss CVR => wpostats.com

## shape perf culture

- make everybody aware and care of perf, everybody's biz
- feel encouraged to say “no” to things slowing down your site
- celebrate success
- Etsy: announce performance heroes every month on their blog
- be transparent (again Etsy: Site Performance Report)

## perf = perception + respect

- perception = subjective

## how long does it take for users to interact with page

- treat speed as feature (ilya grigorik)
- optimize from user’s perspective, not with your company’s fast internet conn.
- wireframing for perf
  - perf point system
  - use WebPageTest for insights (film strip of loading)
  - measurable perf modules (MPM)
    - low impact = 1 point
    - medium impact = 2 point
    - high impact = 6 point
	- load important stuff first, use PPS

## measure first, then optimize

- set perf budget
- check competitors
- speed index (avg. time at which vis. parts are displayed)
- pagespeed score (Google)
- speedcurve (Steve Souders)

## the browser

- render workflow (HTML, CSS, blocking JS, render tree, layout, paint)
- determine critical rendering path
  - bookmarklet for optimizing CRP
- know how the browser renders (order)

@TODO: see photo

- 14 kB rule, serve most important content first
  - 14 kB in first roundtrip
  - most important styles inline
- script best practices
  - use `defer` and `async`
  - put script in the bottom

## Reduce bytes

- minify HTML, CSS, JS
- compress images
- avoid web fonts (or consider web font loader)
- use Gzip techniques

## reduce HTTP requests

- concatenate
- use libs only when needed
- sprite
- data URIs

=> *what abozt http2*

## latency

- reduce requests
- high latency on mobile
- reduce polling
- send important styles in first 14 kB
- remove reirs
- use offline storage techniques
- use considerations
- use HTTP/2

## make friends with the server

- Gzip your assets
- cache stuff appropriately

## tame mobile

- dont make the user pay for bad perf
- reduce requests and DNS lookups
- remember batteries
- consider offline
- test on real device

## Automate perf routines

- task runners (Grunt, Gulp, Maven, Ant…)
  - include perf APIs in CI

## avoid yo-yo-effect

- constant measuring, monitoring
- automation incedibly helpful by triggering appropr warnings

> Browsing should be as simple and fast as turning a page in a mag. (Larry Page)

https://twitter.com/jaronbarends/status/784308180041871361
