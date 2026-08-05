# Asset Quality Audit — 2026-08-05

## Scope

All 95 public-safe assets currently represented in the app were matched by exact filename against promoted/approved sources in `05_VISUAL_ASSETS/`. No prompt sidecars or private originals were copied.

## Result

- Audited: **95 / 95**
- Approved source found: **95 / 95**
- Publication-ready under the minimum-resolution policy: **80**
- Blocked pending a higher-resolution approved source: **15**
- Base64 images remaining in `data.js`: **0**
- Navigation thumbnails: separate WebP files, maximum 512 px on the longest edge
- Publication files: separate files under `assets/publish/`

## Resolution policy

| Use | Minimum |
|---|---|
| Chapter covers and scenes | 1600 px on longest edge |
| Character/environment/diagram raster references | 1600 px on longest edge |
| Instagram feed 4:5 | 1080×1350 |
| Quote cards 1:1 | 1080×1080 |
| Stories/Reels 9:16 | 1080×1920 |
| Content thumbnails 16:9 | 1280×720 |
| Library navigation thumbnails | max 512 px longest edge; never used for publication |
| SVG publication sources | vector; separate raster thumbnail |

## Blocked assets

| Asset | Real source | Requirement | Reason |
|---|---:|---|---|
| `CHR-001_vesper_kole_v1.png` | 1536×1024 | Cover/scene/reference raster — minimum 1600 px on longest edge | Higher-resolution approved source required |
| `CHR-002_augustin_reyes_v1.png` | 1536×1024 | Cover/scene/reference raster — minimum 1600 px on longest edge | Higher-resolution approved source required |
| `CHR-003_nneka_osei_v1.png` | 1536×1024 | Cover/scene/reference raster — minimum 1600 px on longest edge | Higher-resolution approved source required |
| `CHR-004_teodora_vance_v1.png` | 1536×1024 | Cover/scene/reference raster — minimum 1600 px on longest edge | Higher-resolution approved source required |
| `ENV-002_mouth_v1.png` | 1536×1024 | Cover/scene/reference raster — minimum 1600 px on longest edge | Higher-resolution approved source required |
| `ENV-003_shaft_v2.png` | 1536×1024 | Cover/scene/reference raster — minimum 1600 px on longest edge | Higher-resolution approved source required |
| `ENV-004_landing_one_v2.png` | 1536×1024 | Cover/scene/reference raster — minimum 1600 px on longest edge | Higher-resolution approved source required |
| `ENV-005_maintained_stair_v1.png` | 1536×1024 | Cover/scene/reference raster — minimum 1600 px on longest edge | Higher-resolution approved source required |
| `ENV-006_freight_shaft_v2.png` | 1536×1024 | Cover/scene/reference raster — minimum 1600 px on longest edge | Higher-resolution approved source required |
| `ENV-007_water_course_v1.png` | 1536×1024 | Cover/scene/reference raster — minimum 1600 px on longest edge | Higher-resolution approved source required |
| `ENV-008_uplink_panel_v1.png` | 1536×1024 | Cover/scene/reference raster — minimum 1600 px on longest edge | Higher-resolution approved source required |
| `CH-001_scene-01_mouth_closure_candidate.jpg` | 1448×1086 | Cover/scene/reference raster — minimum 1600 px on longest edge | Higher-resolution approved source required |
| `CH-003_scene-01_three_routes_candidate.jpg` | 1536×1024 | Cover/scene/reference raster — minimum 1600 px on longest edge | Higher-resolution approved source required |
| `CH-004_scene-01_eighty_one_millimetres_candidate.jpg` | 1448×1086 | Cover/scene/reference raster — minimum 1600 px on longest edge | Higher-resolution approved source required |
| `CH-005_scene-01_after_transmission_candidate.jpg` | 1448×1086 | Cover/scene/reference raster — minimum 1600 px on longest edge | Higher-resolution approved source required |


## Architecture changes

- `data.js` stores metadata and relative paths only.
- `thumbnailSrc` always points to `assets/thumbs/`.
- `publicationSrc` points to `assets/publish/` only when the asset passes the policy.
- `publicationSrc` is `null` for blocked assets.
- `width` and `height` now reflect the decoded approved source.
- The download action uses `publicationSrc`, never `thumbnailSrc`.
- ZIP exports omit blocked media and include a `BLOCKED_ASSETS.txt` explanation.

## Approval evidence

The current `ASSET_REGISTRY.md` states that Rodrigo approved the complete Cycle One visual/social package on 2026-08-04. The audit therefore treats approval as confirmed and blocks only on technical resolution.
