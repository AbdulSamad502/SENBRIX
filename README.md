# SENBRIX – Landing Page

Single-page marketing website for **SENBRIX**, a wholesale supplier of construction materials
(cement, steel, sand, bricks, blocks and more). *Building a Stronger Tomorrow.*

Pure HTML, CSS and a few lines of JavaScript — no build step, no dependencies. Fast, mobile-first and SEO-ready.

## Features

- Sections: header and hero, About, Products (11 items), Works & Projects, Why SENBRIX, FAQ, Contact, Footer
- "Ask for price" buttons that open WhatsApp with the product name pre-filled
- Quotation form that sends the details to WhatsApp or email (no backend or database)
- Floating WhatsApp button (desktop) and a Call / WhatsApp bar (mobile)
- SEO: meta tags, Open Graph, JSON-LD (LocalBusiness + FAQ), semantic headings
- Terms & Conditions and Privacy Policy pages, plus a custom 404 page
- Optimised WebP images, lazy loading, long-term caching headers (`netlify.toml`)

## Project structure

```
index.html        Main landing page (HTML + CSS + JS in one file)
terms.html        Terms & Conditions
privacy.html      Privacy Policy
404.html          Not-found page
netlify.toml      Netlify config (publish dir, cache + security headers)
robots.txt        Crawler rules
assets/           Logo, favicon, product / project photos, legal.css
```

## Run locally

Just open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 8000
# then open http://localhost:8000
```

## Edit the business details

In `index.html`:

| What | Where |
| --- | --- |
| WhatsApp number | `WA_NUMBER` in the script at the bottom, plus the `wa.me/91…` links (find and replace) |
| Email | `EMAIL` in the script, plus the `mailto:` links |
| Phone numbers | `tel:` links in the contact section and footer |
| Instagram | the `instagram.com/senbrix…` links |
| Products | the `pcard` blocks inside `#products` |

To replace a photo, overwrite the file in `assets/` with the same name (WebP, about 800×600 for products).

## Deploy to Netlify

1. Push this repo to GitHub.
2. In Netlify: **Add new site → Import an existing project → GitHub**, pick this repo.
3. Build command: *(leave empty)* · Publish directory: `.` (already set in `netlify.toml`) → **Deploy**.

Every `git push` to the main branch then redeploys automatically.

## Before going live – checklist

- [ ] Confirm the WhatsApp number and Instagram link
- [ ] Add the real Facebook link (removed for now) if the company has a page
- [ ] Replace stock photos with the company's own
- [ ] Add `canonical`, `og:url` and an absolute `og:image` once the final domain is known (see the TODO comment in `<head>`)
- [ ] Have the Terms & Privacy pages reviewed; add the registered address, GST number and jurisdiction city
- [ ] Submit the site in Google Search Console

## Credits

Stock photos from [Pexels](https://www.pexels.com) (free to use). Brand names and logos shown belong to their respective owners.

© SENBRIX. All rights reserved.
