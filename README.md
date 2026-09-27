# Kretz – pre-release page

"Coming soon" page for kretz.no, hosted on GitHub Pages while we test it.

- `index.html` – the page (exported from Claude Design)
- `i18n.js` – Norwegian/English text
- `config.js` – EmailJS keys for the "Meld interesse" form
- `vendor/` – React, served locally

## Email (EmailJS)

The form sends through [EmailJS](https://www.emailjs.com) (free: 200 emails/month).
The recipient is set in the EmailJS template, so switching from the test address to
kontakt@kretz.no needs no code change.

Template variables sent by the page: `{{subject}}`, `{{klubbnavn}}`, `{{idrett}}`,
`{{epost}}`, `{{melding}}`, `{{message}}` (the full email text).

## Moving to kretz.no

1. Add a `CNAME` file containing `kretz.no`.
2. In Domeneshop DNS, point `kretz.no` A records to 185.199.108.153, 185.199.109.153,
   185.199.110.153, 185.199.111.153, and `www` CNAME to `viktordy.github.io`.
3. Settings → Pages → Custom domain: `kretz.no`, then tick "Enforce HTTPS".
4. Add `https://kretz.no` to the allowed origins in EmailJS.
