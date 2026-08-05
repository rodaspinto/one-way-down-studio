# ONE WAY DOWN — Project Status

Updated: 2026-08-05

## Production

- Version: unversioned baseline
- Published commit: `b1faf20f1891e428cd0b8facdb5c02c36a5b8226`
- GitHub Pages: reachable for public-safe review
- Launch state: `BLOCKED`
- Offline/install state: `BLOCKED`

The application remains online because normal network navigation works. It must
not be marketed as reliably installable until the service-worker issue is fixed
and real-device checks pass.

## Work in progress

- Issue: [#1 — establish audited collaboration baseline](https://github.com/rodaspinto/one-way-down-studio/issues/1)
- Change type: documentation only
- Development state: `IN_REVIEW`
- Application behavior and public data: unchanged

## Confirmed baseline

- Both independent audits found no leak beyond the authorized public chapter
  range.
- The 14 areas rendered at desktop, tablet, and 390 px mobile viewports.
- Core editorial operations and exports worked during the audit.
- Produced audiovisual material may be `READY_FOR_REVIEW`; this does not mean
  `APPROVED` or `PUBLISHED`.
- Working Patreon labels are `Free follower`, `GROUND CREW`, `RELAY`, and
  `CHARTER`; all remain hypotheses and blocked from public promises until
  validation and owner approval.

## Blocking issues

1. Broken service-worker pre-cache path.
2. Invalid backup data can be persisted before validation.
3. Route fallback uses the same incorrect JSZip path.
4. Accessibility gaps in dialogs, focus, labels, mobile controls, and sizing.
5. No automated tests or continuous integration.
6. Editorial timezone is not applied consistently in JavaScript.
7. Physical Safari/iPhone installation has not been verified.

## Next three priorities

1. Merge the reviewed documentation baseline.
2. Repair PWA/404 resources and add a smoke check.
3. Validate and migrate backup data safely before persistence.

## Review gates

- Latest Claude review: independent privacy/editorial audit completed; public PR
  review pending
- Latest Codex review: technical/UX audit completed; documentation PR validation
  pending
- Latest owner decision: roadmap and documentation-only first PR approved;
  final PR approval pending
