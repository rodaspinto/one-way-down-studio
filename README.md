# ONE WAY DOWN — Content Studio

Public-safe editorial operations app for **ONE WAY DOWN**.

## Live app

<https://rodaspinto.github.io/one-way-down-studio/>

The live app is suitable for public-safe review and editorial work. It must not
yet be presented as launch-ready or reliably installable offline: the current
service-worker pre-cache contains a broken JSZip path. See
[`PROJECT_STATUS.md`](PROJECT_STATUS.md).

## Included

- 14 operational areas;
- 95 public-safe image previews embedded in `data.js`;
- 14 pre-launch post records;
- seven authorized public chapter records;
- calendar and post editing;
- ZIP, CSV, ICS, and JSON backup/export operations;
- browser-local persistence;
- a mobile-first Ground Control interface.

## Repository structure

The application is intentionally static and lives at the repository root:

- `index.html` — application shell;
- `styles.css` — Ground Control visual system;
- `app.js` — interaction and editorial logic;
- `data.js` — public-safe records and embedded previews;
- `jszip.min.js` — local ZIP generation;
- `manifest.webmanifest`, `sw.js`, and `icon.svg` — PWA resources;
- `404.html` — GitHub Pages route fallback;
- `docs/audits/` — public-safe audit records and roadmap.

GitHub Pages publishes directly from the repository configuration. There is no
Pages workflow file in this baseline.

## Privacy boundary

This is a public repository. Deliberately excluded:

- private canon and unrevealed story material;
- full manuscripts and unreleased chapters;
- future votes, consequences, and secret continuity;
- private cloud links, IDs, paths, or backups;
- private audio/video originals and licensing evidence;
- credentials, tokens, and personal data.

If a fact is not supported by an authorized public source, record it as
`BLOCKED` or `UNKNOWN`; do not infer it.

## Local data

Browser edits are stored in `localStorage`. Export a JSON backup before clearing
browser data or changing devices. Until schema validation and rollback are
implemented, import only backups exported by the same app version.

## Status language

- `DRAFT` — incomplete and not ready for review;
- `IN_REVIEW` — actively being checked;
- `READY_FOR_REVIEW` — produced, but not approved;
- `APPROVED` — explicitly approved by the project owner;
- `SCHEDULED` — approved and assigned a publication time;
- `PUBLISHED` — confirmed live on the destination platform;
- `BLOCKED` — cannot advance until the stated condition is resolved;
- `ARCHIVED` — retained for history, not active.

Existence is not approval. A produced audio or video may be
`READY_FOR_REVIEW` while still being neither `APPROVED` nor `PUBLISHED`.

## Collaboration

Read [`AGENTS.md`](AGENTS.md) before changing this repository.

Every material change follows:

1. a GitHub Issue with evidence and acceptance criteria;
2. a dedicated branch;
3. a draft pull request;
4. independent Claude and Codex review;
5. explicit owner approval;
6. merge and post-deployment verification.

Never commit directly to `main`.
