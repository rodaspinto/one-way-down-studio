# Joint Baseline and Roadmap

Date: 2026-08-05

Audited commit: `b1faf20f1891e428cd0b8facdb5c02c36a5b8226`

## Joint verdict

The application passed the public privacy boundary and may remain online for
review. It is not yet ready to be presented as a reliable installable PWA or a
completed launch system.

Claude and Codex agree that:

1. the public dataset contains only the authorized chapter range;
2. no private cloud reference, credential, or private original was found;
3. public quotations checked during review are faithful;
4. unknown states remain blocked;
5. repository documentation did not match the real structure;
6. launch-critical technical and semantic work remains.

## Reconciled decisions

### Audiovisual material

Private evidence confirms that the first authorized chapter has produced audio
and video. The truthful public state is `READY_FOR_REVIEW`, not `APPROVED` or
`PUBLISHED`. A follow-up data migration should replace booleans with explicit
production states.

### Patreon

The app placeholders are unsupported. The authorized working labels are
`Free follower`, `GROUND CREW`, `RELAY`, and `CHARTER`, all still classified as
hypotheses and blocked from promises until validation and owner approval.

## What must be preserved

- the 14-area Ground Control workflow;
- mobile-first and desktop usability;
- public-safe previews rather than private originals;
- browser-local operation without invented platform integrations;
- visible blocking of unknown or unconfirmed states;
- the static architecture until a real migration case is approved.

## Roadmap

### Documentation baseline

- correct repository paths and deployment claims;
- add governance, status, changelog, audits, and PR checklist;
- change no application behavior or public data.

### Critical corrections

1. Repair service-worker and route-fallback resources.
2. Add a PWA/resource smoke check.
3. Validate versioned backup data before persistence.
4. Add migration and rollback behavior.

### Trust and semantics

1. Replace ambiguous audiovisual booleans with explicit states.
2. Align Patreon working labels while keeping them blocked.
3. Correct dialog, focus, labels, keyboard behavior, and mobile target sizing.
4. Add automated tests and continuous integration.
5. Apply `Europe/Lisbon` explicitly.

### Release verification

- test physical Safari/iPhone installation and standalone behavior;
- verify Pages after every merged fix;
- approve publication copy, platforms, schedule, licensing, and rating
  separately;
- never equate a produced asset with publication approval.

## Proposed release sequence

- `v2.0.1` — critical PWA, route fallback, and data-integrity fixes;
- `v2.1.0` — trust, explicit states, accessibility, tests, and transparency;
- `v2.2.0` — separately reviewed visual and operational improvements.

Versions remain proposals until the owner approves release numbering.

## Success criteria

- no private material in repository history or public output;
- service worker installs with every core resource available;
- malformed imports cannot corrupt persisted state;
- all 14 areas pass automated and manual smoke checks;
- keyboard and screen-reader semantics meet the agreed baseline;
- status text reflects evidence;
- every merge has independent review and owner approval.
