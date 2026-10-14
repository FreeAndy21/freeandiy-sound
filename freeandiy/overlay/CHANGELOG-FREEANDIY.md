<!-- Modified-by: FreeANDIY (Free Andy Agency), 2026. New file, not part of upstream SoundCraft. -->
# FreeANDIY Sound: changes from upstream SoundCraft

This file lists what the FreeANDIY fork changes in SoundCraft (Apache-2.0 section 4(b)). The
exact changes are generated from `freeandiy/` (see `NOTICE`); `git diff upstream-main main`
shows every changed file.

## Unreleased

### Branding
- Product name **FreeANDIY Sound** everywhere users see it: window titles, About, messages,
  installers, desktop entries, the web page and the CLI.
- Application id `agency.freeandy.sound` (was `ai.storyteller.soundcraft`), so FreeANDIY builds
  install next to SoundCraft.
- Executables `freeandiy-sound` and `freeandiy-sound-cli`; the cargo packages keep their names.
- New app icon set and in-app mark (the angel Andy, Free Andy Agency) and DMG background.
- Light and dark palettes in FreeANDIY's paper-and-ink print look (no soft shadows, the
  stamp-rose accent). Meters, solo, mute, record, automation and the counter keep upstream's
  colours.
- UI font IBM Plex Sans (OFL 1.1) on the desktop; the system fonts stay as fallbacks.

### Removed
- The ArtCraft name, wordmark and logos (`docs/brand/`), as their terms require of forks.
- The ArtCraft Discord and website links (About, installers, desktop metadata).
- Upstream's release and platform workflows, which call ArtCraft's shared actions; ours are
  `freeandiy*.yml`.

### Added
- About: the app's mark, attribution to upstream SoundCraft and the Free Andy Agency seal, and a
  link to our issue tracker.
- `NOTICE` section and `ATTRIBUTION.md` rows for FreeANDIY's assets and fonts; packages, the
  Windows portable ZIP included, now ship `NOTICE`, `ATTRIBUTION.md`, the font licences and the
  brand terms.
