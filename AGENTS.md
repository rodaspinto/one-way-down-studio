# ONE WAY DOWN — Collaboration Contract

## Authority and mission

The project owner is the final authority for canon, publication, material visual
changes, commercial decisions, and merges.

Claude and Codex maintain a stable, public-safe editorial application without
inventing facts, exposing private material, or silently changing what is already
working.

## Sources of truth

Use this order:

1. explicit owner decision;
2. authorized private sources, only inside their permitted environment;
3. authorized public-safe production sources;
4. `main` as the currently published public application;
5. Issues, pull requests, audits, changelog, and project status;
6. chat context only as temporary context.

If a fact is not supported by an authorized source, mark it `UNKNOWN` or
`BLOCKED`. Never turn an inference into a fact.

## Public-repository boundary

Never commit:

- private canon, manuscripts, or unreleased chapters;
- future votes, consequences, or secret continuity;
- private cloud links, IDs, paths, or backups;
- private media originals or licensing evidence;
- credentials, tokens, cookies, personal data, or hidden metadata.

If in doubt:

1. stop the public patch;
2. classify the item as `BLOCK_PRIVACY`;
3. describe the category of risk without revealing the content;
4. request an owner decision.

## Roles

### Claude

- narrative and continuity guardian;
- editorial requirements and information architecture;
- state, wording, privacy, and spoiler review;
- independent reviewer of Codex work.

### Codex

- software engineering, architecture, UI/UX, and accessibility;
- testing, performance, client security, Git, and GitHub Pages;
- Ground Control interface consistency;
- independent technical reviewer of Claude proposals.

Neither agent changes canon or substitutes for owner approval.

## Required workflow

Every material change follows:

1. **Issue** — problem, evidence, impact, proposal, alternatives, privacy and
   data impact, acceptance criteria, tests, risk, and rollback.
2. **Branch** — never work directly on `main`; use a narrow branch such as
   `codex/issue-<n>-description` or `claude/issue-<n>-description`.
3. **Implementation** — one controlled concern, minimal dependencies, reversible
   diff.
4. **Draft PR** — link the Issue and complete the repository checklist.
5. **Independent review** — Claude and Codex each declare
   `APPROVE`, `APPROVE_WITH_CHANGES`, `REQUEST_CHANGES`, or `BLOCK_PRIVACY`.
6. **Owner gate** — material changes require explicit owner approval.
7. **Merge and verify** — merge only after all gates, then verify Pages and
   update `CHANGELOG.md` and `PROJECT_STATUS.md`.

Never force-push `main`, erase history, combine unrelated changes, or perform a
broad rewrite without an approved migration and rollback plan.

## Preserve the working product

The app has 14 operational areas:

1. Today
2. Visual Library
3. Chapters
4. Content
5. Calendar
6. Patreon
7. YouTube
8. Social Media
9. Votes
10. Production
11. Downloads
12. Metrics
13. Audit
14. Settings

Navigation, mobile menu, previews, filters, asset modal, favorites, public
chapters, post editing, calendar, CSV, ICS, ZIP, JSON backup/import, local
persistence, visible states, iPhone layout, desktop layout, and PWA behavior must
not regress.

## Data and status rules

- Validate external or imported data before persistence.
- Do not change localStorage shape without `schemaVersion`, migration, and
  rollback.
- Never send local browser data to GitHub automatically.
- Existence does not imply approval.
- Use the status definitions in `README.md`.
- Working Patreon labels are hypotheses until validated and owner-approved.

## Ground Control visual rules

- Void black `#0A0C0D`;
- panel `#14181B`;
- secondary panel `#1B2024`;
- structural grey `#4A5158`;
- cold light `#B9CBD6`;
- amber `#E09A3E`;
- salt white `#E8E4DC`.

Amber is an operational accent. Preserve dense, precise, legible interfaces,
limited rounding, accessible contrast, adequate touch targets, reduced-motion
support, and the Vandry Program / Ground Control identity. Avoid generic SaaS
styling, decorative neon, and unnecessary frameworks.

## Validation baseline

For code changes, test at minimum:

- page load and console;
- all 14 areas;
- 390×844, 375×667, 768×1024, and 1440×900;
- mobile menu and modal keyboard/focus behavior;
- create/edit post;
- JSON backup and safe import;
- CSV, ICS, and ZIP;
- localStorage persistence and migration;
- service-worker resources and offline behavior;
- privacy scan of the complete diff.

Documentation-only PRs may mark behavior checks as not applicable, but must run
link/path checks, `git diff --check`, and a privacy scan.

## Definition of done

A task is complete only after its Issue criteria pass, the branch and PR are
reviewed, privacy is cleared, the owner approves when required, the change is
merged and deployed, the live app is verified, and status documentation is
updated. Creating a patch is not completion.
