# Zesto Sports Flooring Website

Official website codebase for Zesto Sports Flooring.

## Branch workflow
- `main` = production
- `develop` = active development / Cloudflare preview
- Review preview deployments before promotion to `main`.

## Foundation V1 architecture

```text
public/
  index.html
  products.html
  product.html
  projects.html
  image-credits.html
  404.html
  assets/
    css/styles.css
    js/site.js
    js/products.js
    images/zesto-logo.svg
wrangler.jsonc
```

The original single-file browser prototype has been refactored into maintainable assets while preserving the established Zesto visual direction.

## Product pages
`product.html?slug=<slug>` renders product-specific content from `assets/js/products.js`, so solution content can evolve without duplicating full page templates.

## Deployment
Cloudflare Workers Static Assets deploys `./public`. Non-production branch builds are used for preview/testing; `main` is reserved for approved production releases.

## Content policy
Representative sports imagery may be used temporarily. Verified Zesto project case studies should only be published with approved original project photography and project data.

Temporary sports photography is loaded from credited Pexels sources during development. Replace it progressively with approved Zesto originals before production launch.
