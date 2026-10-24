# Phishing Education Page

A single-page "teachable moment" shown to staff who click a link in a simulated phishing email as part of Holmesglen security awareness training. Instead of an error or a scolding, the page reassures the reader they're safe and explains:

- what happened (a routine-looking email led to a fake login page)
- the warning signs in that message
- a quick check to apply to any message
- how to stop, check and report suspicious messages
- how to protect their account (passphrases, MFA)
- trusted resources from the Australian Cyber Security Centre and Scamwatch

**Live page:** https://osipovaelena.github.io/phishing-education-page/

## Project structure

```
docs/
├── index.html   # the page — self-contained HTML/CSS, no build step
└── .nojekyll    # serve files as-is, skip Jekyll processing
```

The page has no dependencies beyond Google Fonts (Spectral and Inter), supports light and dark mode, and is responsive down to phone widths.

## Preview locally

Open `docs/index.html` directly in a browser, or serve the folder:

```bash
python3 -m http.server --directory docs 8000
```

Then visit http://localhost:8000.

## Deploy to GitHub Pages

1. Push to the `master` branch on GitHub.
2. In the repository, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to *Deploy from a branch*.
4. Choose branch `master` and folder `/docs`, then **Save**.

GitHub publishes the site at `https://osipovaelena.github.io/phishing-education-page/` within a minute or two, and redeploys on every push to `master`.

## Using it in a phishing simulation

Point your simulation platform's landing-page / redirect URL at the published page. To customise the content (organisation name, reporting address, linked resources), edit `docs/index.html` directly.
