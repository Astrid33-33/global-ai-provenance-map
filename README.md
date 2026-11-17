# AI Provenance Atlas

A responsive, English-language static website comparing AI-generated content provenance rules by jurisdiction and media type. The first release includes China, the European Union, California, South Korea, and India, with separate summaries for text, images, audio, and video, plus a dedicated comparison of their technical standards and implementation pathways.

The visual direction is an editorial research brief: white and warm-gray surfaces, restrained blue and ochre accents, Source Serif 4 headings, Inter body text, generous whitespace, and simple rules instead of cards or dashboard effects. It references information architecture found in Berkeley research projects and does not use Berkeley's logo or claim affiliation.

## Run locally

Open `index.html` in a browser. The site has no build step or runtime dependency. Fonts load from Google Fonts when online; system font fallbacks are included.

## Publish with GitHub Pages

1. Create a GitHub repository and upload the contents of this folder.
2. In the repository settings, open **Pages** and set the source to **GitHub Actions**.
3. The workflow in `.github/workflows/pages.yml` publishes the site after a push to `main` (or when run manually).

The published site is static. All policy summaries and source links live in `app.js`, so additional jurisdictions can be added in the `regions` object. Keep source URLs, effective dates, scope and exceptions with each summary. Use “not found / not disclosed” rather than inferring that no obligation or technology exists.

## Content and limitations

- The map renders immediately with an offline locator map; if boundary data is reachable, it upgrades to a country-by-country map. The map is intentionally resilient when third-party data sources are unavailable.
- Summaries distinguish visible disclosure from machine-readable or metadata provenance and from user-facing detection tools.
- South Korea and India are included with source notes about scope, implementation guidance, and enforcement timing; their laws do not map identically across all four media.
- The technical-standards table separates China's mandatory GB 45438-2025, the EU's binding outcome and voluntary Code of Practice, South Korea's law/decree and implementation guidance, India's intermediary rules, and California's statutory criteria and later large-platform duty.
- Rules can depend on provider size, role, intended use, audience, exceptions, and implementation date. This site is an informational tracker, not legal advice.
- Initial source review date: November 2026.

## Files

- `index.html` — English page structure and accessible landmarks
- `styles.css` — responsive editorial presentation
- `app.js` — jurisdictions, modality filters, legal matrix, standards comparison, and source links
- `.github/workflows/pages.yml` — GitHub Pages deployment workflow
