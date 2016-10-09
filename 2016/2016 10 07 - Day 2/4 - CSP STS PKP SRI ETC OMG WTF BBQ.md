# CSP STS PKP SRI ETC OMG WTF BBQ

🗣 [Scott Helme](https://scotthelme.co.uk/)  
[@Scott_Helme](https://twitter.com/Scott_Helme)

## HTTPS

- Built in HTTP/2
  - Use it for a nice performance boost
- Powerful browser features
  - Geolocation API
  - `getUserMedia()`
  - AppCache
- Brotli compression 🍞
  - Better than Gzip, HTTPS-only
- SEO boost according to Google
- Enables all the cool stuff like PWA, AMP etc.
- Security evolved over time
- Browser support for new HTTPS feature: you shouldn’t care, it falls back to old style 👍🏼

➡️ serve your content over HTTPS

## Content Security Policy (CSP)

- Bad: Content injection, malicious script tag et al. (XSS)
- Good: CSP was built to fix that
- It’s a HTTP header with a policy of defined sources (`image-src`, `script-src` and more)
- Helps finding and fixing mixed content
  - `block-all-mixed-content` prevents warnings, but also mixed content, haha!
  - Use `upgrade-insecure-requests` which tries to upgrade HTTP content on HTTPS pages
  - Detection: `Content-Security-Policy-Report-Only` header, useful for migrations and testing (see [report-uri.io](https://report-uri.io/))
    - Report URIs send you a report of violated directives

## HTTP Strict Transport Security (HSTS)

- Flow without HSTS: `http:` ➡️ `301 https:` ➡️ `https:`
- Flow with HSTS:
  - SSL/TLS stripped
  - Browser defaults to HTTPS
- `Strict-Transport-Security` HTTP header
  - Required: `max-age`
- Performance gain due to reduced redirects

## HTTP Public Key Pinning (HPKP)

- HTTP header with SHA256 hashes of current key and backup
- Hardens certificate chain
- Additional security feature for trust-worthy sites
- Supports report URI, too

## Subresource integrity (SRI)

- Provides 3rd party trust
- Like jQuery from CDN, what if a keylogger gets sent instead of jQuery?
  - Add `crossorigin="anonymous"` and `integrity="sha256-..."` to script (or link) tag
  - Make sure the requested file matches the hash you’ve made of the resource
- Performance boost (hash is used as cache key in some browsers)

```
<script
  src="..."
  crossorigin="anonymous"
  integrity="sha256-[hash]">
</script>
```

> Secure all the things!
