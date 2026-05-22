# Rockwood Kitchens — Website

Production website for Rockwood Kitchens, a bespoke kitchen design studio based in Ballito, KwaZulu-Natal.

**Live site:** https://rockwoodkitchens.co.za
**Studio:** [Mathew Hartley Consulting](https://mathewhartley.consulting)

---

## Stack

Pure static HTML, CSS, and a single Google Fonts call. No JavaScript framework, no build step, no dependencies. Deploys to Cloudflare Pages on every push to `main`.

The visual system (typography, colours, spacing) is documented in `/Rockwood-Kitchens-Corporate-Identity.pdf` (the brand CI document).

## Editing

For text changes:
1. Open the relevant HTML file in any editor
2. Make the change
3. Commit and push to `main`
4. Cloudflare Pages auto-deploys in ~90 seconds

For image changes:
1. Drop the new image into `assets/images/`
2. Update the `src` attribute in the HTML
3. Commit and push

## Project structure

```
.
├── index.html              Home
├── about.html              Philosophy
├── services.html           Services
├── process.html            Process
├── portfolio.html          Portfolio
├── contact.html            Contact (carries the Zoho form)
├── assets/
│   ├── site.css            Design system stylesheet
│   ├── rockwood-monogram.png
│   ├── rockwood-lockup-light.png
│   └── images/             All photography
├── _headers                Cloudflare Pages security headers
├── _redirects              Legacy URL redirects from modurakitchens.co.za
├── robots.txt
└── sitemap.xml
```

## Zoho form

The contact page contains a Zoho Web-to-Lead form. The form's hidden inputs, action URL, validation scripts, and analytics tracking script are wired to the studio's Zoho CRM and **must not be modified**. Visual styling is applied via the page-level `<style>` block.

If the form needs to be regenerated (e.g. Zoho account migrated), replace the entire form block inside `contact.html` between the `ZOHO WEB-TO-LEAD FORM` comment markers, then re-apply the visual restyling.

## Brand

Composed with intention. · Delivered with care.
