## LOG

### 2026-07-01 — scrub molequla brand + fix corpus paths

- Removed every "molequla" mention from the 4 ports (`roots/kairos.{c,go,rs,js}`): ckpt names → `kairos.ckpt` / `kairos_ckpt.json`, swarm dir → `~/.kairos/swarm` (consistent across c/go/rs), UI/log strings → `kairos`, JS class `MolequlaDB` → `KairosDB`, banners. Shared function identifiers kept. `grep -i molequla` over the 4 ports + README = 0.
- Realigned the `KAIROS.RS` box banner (`roots/kairos.rs:3297`).
- Default corpus path was `"nonames.txt"` (file absent) in all 4 ports → now `"kairos.txt"` (the main-Kairos container). Element runs unchanged: `--element earth/air/water/fire` → `nonames_<element>.txt` (files present). README logo → `assets/kairos.jpg` (present).
