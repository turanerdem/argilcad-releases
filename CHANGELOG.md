<div align="right">

🇹🇷 [Türkçe](CHANGELOG.tr.md)

</div>

# Changelog

All notable changes to ArgilCAD will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-07-25

The first public release of ArgilCAD.

### Added

- **Text-to-CAD generation** — describe the part you need in plain language and
  get back a real parametric 3D model, not a mesh.
- **Multiple AI providers** — generate using models from Anthropic, OpenAI,
  Google Gemini and xAI. The model list is configuration-driven, so new models
  can be made available without waiting for an app update.
- **Built-in code editor** — every model is genuine [Build123d](https://build123d.readthedocs.io)
  Python. Open the generated code, edit it freely, and re-run it to update the
  model — the full power of the CAD kernel stays in your hands.
- **Multiple view modes** — inspect your model shaded with edges, shaded without
  edges, as a wireframe, or in X-ray.
- **One-click technical drawings** — turn a model into a technical drawing with a
  single button, at no credit cost. *(Experimental — output may need review.)*

### Platforms

- macOS 11 or later on Apple Silicon (M1 or newer). Intel Macs are not supported
  yet; support is planned for a future release.
- Windows 10 / 11 (64-bit).

<!--
Template for future releases:

## [X.Y.Z] - YYYY-MM-DD

### Added
- New features

### Changed
- Changes in existing functionality

### Fixed
- Bug fixes
-->
