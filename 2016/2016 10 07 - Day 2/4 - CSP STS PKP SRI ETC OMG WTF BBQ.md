# CSP STS PKP SRI ETC OMG WTF BBQ

🗣 [Scott Helme](https://scotthelme.co.uk/)  
[@Scott_Helme](https://twitter.com/Scott_Helme)

## HTTPS

- HTTP/2
  - nice perf boost
- powerful browser features
  - Geolocation API
  - `getUserMedia()`
  - AppCache
- Brotli compression
  - better than Gzip, HTTPS-only
- SEO Boost (acc. to Google)
- PWA, AMP etc.
- => serve content over HTTPS
- security evolved over time
- browser support for new feature: don't care, fallbacks to old style :-)

## CSP

- content injection, malicious script tag et al. (XSS)
- CSP was built to fix that
- HTTP header with a policy of defined sources (`image-src`, `script-src` and more)
- mixed content
  - `block-all-mixed-content` prevents warnings, but also mixed content, haha!
  - so for HTTP content on HTTPS page use `upgrade-insecure-requests`
  - detection: `Content-Security-Policy-Report-Only` header, useful for migrations and testing (see report-uri.io)

## HSTS

- without HSTS
  - http: => 301 https: => https:
- with HSTS
  - SSL/TLS stripped
  - browser defaults to HTTPS
- `Strict-Transport-Security`
- required: `max-age`
- performance gain due to reduced redirect

## PKP

- SHA256 hashes of current key and backup
- ensures cert chain
- supports report URI

## SRI

- provides 3rd party trust
- like jQuery from CDN, what if a keylogger gets sent instead of jQuery?
  - add `crossorigin="anonymous"` and `integrity="sha256-..."` to script (or link) tag
- performance boost (hash used as cache key)

> Secure all the things!
