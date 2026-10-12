# FinancialPhilosopher.net

A single-page static website. There is no build step or server code: upload the
contents of this folder to any web host and `index.html` is the home page.

```
index.html              The whole site: content, styles, and scripts
images/logo-mark.png    Book-and-glasses logo mark (transparent background)
images/austin-mall.jpg  Hero portrait
images/mall-family.jpg  Family photo
images/cfp-logo.png     CFP® certification mark (unaltered color)
```

Fonts load from Google Fonts. Everything else is in this folder.

## Hosting

Any static host works: Netlify, Cloudflare Pages, GitHub Pages, Squarespace or
Wix (custom code), or the hosting that comes with your domain registrar. Point
FinancialPhilosopher.net at the host and upload this folder.

To preview locally, open `index.html` in a browser.

## Common edits (all in index.html)

**Seasonal quotations.** Search for `const QUOTES`. Each entry is
`["quotation text", "Source"]`. Public domain and Scripture only.

**Adding a new Letter.**
1. Copy the `<div class="reader" id="give-caesar-his-due" ...>` block (just
   below `</main>`), give it a new `id` (for example `id="next-letter-title"`),
   and replace the title, byline, date, and paragraphs. Change `caesar-title`
   to a new unique id in both places in the copy.
2. Add an entry at the top of `const LETTERS` with `title`, `cat`
   (`practical`, `behavioral`, `theological`, `familial`, or `historical`),
   `date`, `url` (`#` plus the new id), and a one-sentence `intro`.
3. Update the "Most recent Letter" panel in the `#letters` section to point to
   the new Letter.

Each Letter has its own link: FinancialPhilosopher.net/#give-caesar-his-due

**Contact form.** The form currently shows visitors their note to copy and
email to Austin.Mall@LPL.com; it does not send anything. To deliver
submissions to the inbox, connect a form service (for example Formspree or
Netlify Forms) in the `/* ---------- Contact form ---------- */` script,
after confirming with LPL compliance how website messages must be archived.

## Before going live

Submit the site and each Letter to LPL compliance for review.
