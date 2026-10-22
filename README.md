# Exccellence Work

Personal-development coaching website for Sabrina Appriou, founder of **Exccellence Work**.

The site is in French. It presents the coaching practice, the method, client stories, qualifications, and ways to get in touch.

## Pages

Open `index.html` in a browser. There is also a `404.html` page for missing addresses.

The home page is a single scrolling page:

- **Le coaching** — what coaching is, and how a session works
- **Accompagnement** — the Exccellence Work method (mental strength, motivation, and listening to emotions), with detail on what it is, who it is for, and the tools used
- **Témoignages** — client feedback
- **Qui je suis** — presentation of Sabrina Appriou
- **Qualifications** — training and areas of expertise
- **Contact** — phone, alternative WhatsApp number, email, guided contact form, and a map

Privacy policy and terms of use open from the footer.

## Contact

- Phone: [06 61 79 46 99](tel:+33661794699)
- WhatsApp (alternative number): [06 11 80 63 96](https://api.whatsapp.com/send?phone=+33611806396)
- Email: [sabrina.appriou@hotmail.fr](mailto:sabrina.appriou@hotmail.fr)

## Tech

- HTML, with page sections filled from `assets/html/`
- [Bootstrap 5](https://getbootstrap.com/) for layout
- Sass sources in `src/scss/` (compiled stylesheet: `css/main.min.css`, plus `css/brand.css` for the wordmark)
- JavaScript modules in `src/js/`, bundled with [Webpack](https://webpack.js.org/) to `js/bundle.js`
- Content data in `src/js/json/data.json`
- [Leaflet](https://leafletjs.com/) for the contact map
- Font Awesome icons

The contact form posts to the mail service set in a `.env` file as `MAILER`. Without that value, the form cannot send, and the error message shows the phone, WhatsApp, and email above.

## Run locally

The page can be opened directly:

```bash
start index.html
```

To rebuild the JavaScript bundle after changing files in `src/js/`:

```bash
npm install
npx webpack --watch false
```

`webpack.config.js` turns watch mode on by default, so pass `--watch false` for a one-off build.
