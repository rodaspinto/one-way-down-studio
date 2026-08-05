# Codex Technical and UX Audit

Date: 2026-08-05

Audited commit: `b1faf20f1891e428cd0b8facdb5c02c36a5b8226`

State: public-safe baseline report

## Scope and method

This audit was completed before repository changes. It covered the published
app, source structure, PWA resources, local persistence, import/export behavior,
console output, and desktop, tablet, and mobile viewports.

No private manuscripts, unreleased chapters, cloud links, original media,
credentials, or licensing evidence were used.

## Passed

- All 14 operational areas opened and rendered.
- No horizontal overflow or normal-path console errors were observed.
- Viewports checked: 1440×900, 768×1024, and 390×844.
- Mobile navigation, visual-library search, persistence, and valid JSON import
  worked.
- ICS, CSV, JSON, and ZIP exports completed.
- Asset, post, and chapter references were internally consistent.
- The dataset contained only the authorized public chapter range.
- Unknown license and readiness states remained visibly blocked.
- No runtime `eval`, remote runtime dependency, or automatic publishing claim
  was found.
- Observed editable values were escaped before HTML insertion.

## Critical findings

### P1 — PWA installation/offline registration fails

`sw.js` pre-caches `./vendor/jszip.min.js`, while the repository publishes
`./jszip.min.js`. The missing response prevents a clean service-worker install.
Normal online navigation hides the failure.

### P1 — invalid backup shape can brick startup

Import merges and persists data before the new shape is proven renderable.
Syntactically valid JSON such as `posts: null` can be saved, after which startup
fails while looking up posts.

Required direction: versioned schema validation, dry-run render or equivalent
structural validation, persistence only after success, explicit migrations, and
automatic rollback.

### P1 — documentation contradicted the repository

The previous documentation described a `src/` tree, vendor subdirectory, and
Pages workflow that do not exist. This PR addresses only that documentation
finding.

### P1 — accessibility gaps

- modal lacks dialog semantics and explicit focus management;
- Escape does not close it;
- tested editor and settings controls lack programmatic label association;
- the mobile menu control lacks an accessible name and expanded state;
- some touch targets and metadata text are undersized.

### P1 — reviewability and automated protection

Key application and data files are compressed into very long lines without a
readable source/build path, tests, or CI checks. Any restructuring must be a
separate, reversible proposal rather than a broad rewrite.

## Secondary findings

- `404.html` uses the old JSZip path.
- `Europe/Lisbon` is displayed but not explicitly applied to every date
  operation.
- The service worker caches without checking `response.ok` and returns the app
  shell for missing resource requests.
- A defensive content-security and referrer policy should be evaluated.
- JSZip provenance and licensing should be documented.
- Physical Safari/iPhone installation, standalone mode, safe areas, and reopen
  behavior still require human device testing.

## Recommended order

1. Establish the reviewed documentation and governance baseline.
2. Repair PWA and 404 resources with an automated resource smoke check.
3. Add safe backup schema validation, migration, and rollback.
4. Correct accessibility and mobile ergonomics.
5. Add automated tests and PR checks.
6. Make timezone behavior explicit.
7. Complete physical iPhone verification before launch claims.
