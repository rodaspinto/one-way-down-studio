# CLAUDE.md — ONE WAY DOWN Content Studio

## Mission

Maintain and improve the public-safe editorial operations PWA for ONE WAY DOWN.

## Absolute privacy boundary

Never commit, infer, reconstruct, expose, or request publication of:

- content from `01_CANON_PRIVATE`;
- full chapter manuscripts;
- CH-008 or CH-009 until explicitly authorized for public release;
- future vote options, consequences, open loops, or unrevealed canon;
- private Google Drive URLs or file IDs;
- unpublished audio/video originals;
- credentials, tokens, personal data, or commercial-license evidence.

## Repository structure

- `src/index.html` — app shell;
- `src/styles.css` — Ground Control design system;
- `src/app.js` — interaction and editorial logic;
- `src/data.js` — public-safe records plus 95 optimized preview images;
- `src/vendor/jszip.min.js` — local ZIP generation;
- `.github/workflows/pages.yml` — GitHub Pages deployment.

## Product rules

- Mobile-first, particularly Safari on iPhone.
- Preserve the Ground Control visual language.
- Every visible button must execute a real action.
- Never claim automatic publication without real platform APIs.
- Never invent dates, metrics, licenses, content, or readiness.
- Missing or unconfirmed material must remain visibly blocked.
- Preserve `Europe/Lisbon` as the editorial timezone.
- Do not replace public-safe previews with private originals.

## Development workflow

1. Read this file and `README.md`.
2. Work on a branch and open a pull request.
3. Test desktop and a 390 px mobile viewport.
4. Verify all 14 navigation areas.
5. Test localStorage, JSON import/export, ZIP, CSV and ICS.
6. Inspect the diff for private material before merging.

## Private handoff

The user may export a JSON backup from the app and share it privately with Claude. Analyze it privately. Do not commit it unless the user explicitly confirms that every field is public-safe.
