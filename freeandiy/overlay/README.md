<!-- Modified-by: FreeANDIY (Free Andy Agency), 2026. Replaces upstream SoundCraft's README. -->
<p align="center">
  <img src="assets/app-icon/freeandiy-sound-1024.png" width="128" alt="FreeANDIY Sound icon">
</p>

<h1 align="center">FreeANDIY Sound</h1>

<p align="center">
  <b>A free, open-source digital audio workstation. Native Rust, runs on macOS, Windows, Linux, FreeBSD and in the browser.</b><br>
  Part of <a href="https://freeandiy.freeandy.agency">FreeANDIY</a>, free creative and office apps by Free Andy Agency.
</p>

---

## About

FreeANDIY Sound records, edits and mixes audio: multitrack editing, a full mixer with plugins
(CLAP, VST3, Audio Units), sends and automation, MIDI, recording and bouncing. It is a native egui
app (no webview), and the web version is the same Rust code compiled to WebAssembly.

Every action is a command, so the app can be driven from a CLI (`freeandiy-sound-cli`), a JSON
control channel or an MCP server.

**FreeANDIY Sound is based on the open-source project
[SoundCraft](https://github.com/storytold/soundcraft) (© ArtCraft Team and contributors,
MIT/Apache-2.0). FreeANDIY is not affiliated with the ArtCraft team.** The workstation itself is
their work; FreeANDIY adds its own branding and packaging, and follows upstream closely.

## Download

Builds for macOS, Windows and Linux are published on the
[Releases](https://github.com/FreeAndy21/freeandiy-sound/releases) page as
`freeandiy-sound-<version>-<os>-<arch>.*`.

## Build from source

Requires Rust (see `rust-version` in `Cargo.toml`).

```sh
cargo run --release -p soundcraft                        # desktop app (binary: freeandiy-sound)
cargo run --release -p soundcraft-cli -- --help          # CLI (binary: freeandiy-sound-cli)
cd apps/soundcraft-web && trunk build --release          # web build (WebAssembly)
```

The crate names keep upstream's `soundcraft-*`, so upstream changes merge cleanly. The developer
documentation in `docs/` is upstream's and still says SoundCraft; upstream's README is kept as
[`docs/upstream-README.md`](docs/upstream-README.md).

## How this fork is made

Everything FreeANDIY changes lives in [`freeandiy/`](freeandiy/): the brand definition
(`branding.toml`, `app.toml`), assets, a handful of small patches and text rules. All other files
are regenerated from upstream SoundCraft by `freeandiy/scripts/regenerate.sh`, so updates from
upstream never conflict. See [`freeandiy/docs/upstream-sync.md`](freeandiy/docs/upstream-sync.md).

Issues with FreeANDIY builds go to
[our tracker](https://github.com/FreeAndy21/freeandiy-sound/issues), not to upstream.

## License

The code is licensed, like upstream, under either of [MIT](LICENSE-MIT) or
[Apache-2.0](LICENSE-APACHE) at your option. See [`NOTICE`](NOTICE) and [`ATTRIBUTION.md`](ATTRIBUTION.md)
for third-party material.

The FreeANDIY and Free Andy Agency names, the angel Andy, logos and app icons are © Free Andy
Agency and **not** covered by the code license; see
[`freeandiy/assets/brand/LICENSE-brand.txt`](freeandiy/assets/brand/LICENSE-brand.txt).

<sub>Avid and Pro Tools are trademarks or registered trademarks of Avid Technology, Inc. in the United States and/or other countries. FreeANDIY Sound is an independent, open-source project and is not affiliated with, sponsored by or endorsed by Avid Technology, Inc.; these names are used only to describe the workflows it is compatible with.</sub>

<sub>Adobe, Photoshop, Illustrator, Premiere Pro, Lightroom, Acrobat, After Effects and InDesign are trademarks or registered trademarks of Adobe Inc. in the United States and/or other countries. FreeANDIY Sound is an independent, open-source project and is not affiliated with, sponsored by or endorsed by Adobe Inc.; these names are used only to describe the workflows it is compatible with.</sub>
