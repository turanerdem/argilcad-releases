<div align="right">

🇹🇷 [Türkçe](CHANGELOG.tr.md)

</div>

# Changelog

All notable changes to ArgilCAD will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.4] - 2026-08-29

A fix-only release, and a required one: in the installed app, downloading a
model, exporting it as a file or a drawing, and deleting it all failed while
everything else looked perfectly healthy.

### Fixed

- **Model downloads, drawing and file exports, and model deletion failed in the
  installed app.** Those requests were sent to a fixed port while the built-in
  engine had started on a different one, so they were refused. The app still
  reported a healthy engine and generated models normally, which made the
  failure look random rather than pointing at its cause. The development setup,
  where the port never changes, was never affected.
- When a request to the engine does fail, the message now names the address that
  was tried instead of reporting a bare connection error.

## [1.0.3] - 2026-08-29

A sketching release: draw a profile with lines, arcs and splines and extrude it
solid or as a hollow wall — alongside cheaper generations and a noticeably
faster editor and viewer.

### Added

- **New sketch drawing tools** — **Line**, **Arc**, **Spline** and **Offset**,
  so a profile no longer has to be built from rectangles and circles alone.
- **Wall mode for extrusions.** A sketch can now keep only the band between the
  outline and its offset, so what you extrude comes out hollow. Set the wall
  thickness, and whether the wall sits inside or outside the outline you drew.
- **Grow or shrink the finished outline** before extruding, without redrawing
  it.
- The code editor now holds back a paid AI edit while the code still has errors,
  instead of spending a credit on an edit that would fail the same way.

### Changed

- **Model generation costs fewer credits.** Work on the same project reuses a
  cached prompt where it can, and the saving goes straight to what you are
  charged.
- **The app is faster where it used to be slowest.** Project and generation
  history open without a pause on large projects, typing in the code editor no
  longer stutters on long files, and the 3D viewer redraws far less while you
  work.

### Fixed

- Downloading a model from Explore and from the generation panel failed.
- Memory kept growing with every feature applied to a model; each edit now
  releases the geometry it replaces.
- A rendering glitch that could leave part of the 3D view uncleared after
  switching views.
- The engine no longer stops answering while a long operation — installing a
  package, for instance — is running: model downloads and status checks go
  through immediately.

## [1.0.2] - 2026-08-13

A stability release: ArgilCAD now starts and runs on setups where it previously
crashed or refused to open, and the 3D camera behaves predictably again.

### Added

- Double-click anywhere on the model to centre the view on that point — the
  fastest way to put the rotation pivot where you are working.
- When the 3D viewer cannot run on a computer, ArgilCAD now explains why, tells
  you what to change, and offers a **Copy diagnostics** button for support
  instead of leaving an empty panel. The rest of the app keeps working.

### Fixed

- **The app no longer crashes on computers with an outdated graphics driver, in
  a virtual machine, or over Remote Desktop.**
- ArgilCAD no longer fails to start when it is installed for all users or in a
  protected folder. Settings and projects are now kept in the standard per-user
  location, and anything from an earlier version is moved there automatically —
  nothing is lost.
- On a computer where more than one person is signed in at the same time, each
  account now works with its own models.
- First launch on Windows is faster and more reliable: the app no longer reports
  that it cannot reach its engine on a fresh install, only to work after
  **Retry**.
- On macOS, permission prompts for the Documents folder no longer prevent the
  app from starting.
- **Reset view** now frames the whole part, whatever its size.
- Switching to the top or bottom view no longer leaves the model tilted with no
  way to straighten it out.
- Zoom now follows the size of your part: you can get close to a small feature
  on a large plate, and a large part is no longer clipped when you zoom out.
- The scroll wheel zooms toward the point under the cursor, so a view that was
  panned away from the part finds its way back.
- The viewer control hints are now one per line and no longer overlap the axis
  indicator in a narrow window.
- When a package with compiled components cannot be installed on macOS, the
  message now says so clearly instead of failing silently.

## [1.0.1] - 2026-08-07

Direct modeling comes to ArgilCAD: shape a model with the mouse, and keep every
bit of the Python behind it.

> ⚠️ This was a required update — older versions can no longer generate models.

### Added

- **Direct modeling tools** — a new **Model** menu with mouse-driven
  operations: fillet, chamfer, push/pull, hole, shell, draft, move, rotate,
  mirror and linear / circular patterns. These are not a separate mode: each
  tool writes real [Build123d](https://build123d.readthedocs.io) code into your
  script, between markers that keep it re-editable. Export the `.py` and it
  still runs.
- **Sketch → extrude / revolve** — draw on any face of the model (rectangles,
  circles, polygons and paths with snapping), then extrude the profile into a
  solid or revolve it around an axis.
- **Three ways to set a number** — drag the arrow handle standing on the picked
  geometry, use the panel slider, or type the value. All three show a live
  preview of the result before you commit.
- **Export** — save your model as STL, STEP or GLB straight from the viewer.
- **Keyboard shortcuts** across the app, with the full list under
  **Help → Keyboard Shortcuts**.
- A toolbar for the code editor.

### Changed

- Faster model generation — the CAD engine is now kept warm in the background
  instead of starting from scratch on every build.
- Clearer, localized error messages when a build fails.
- The app tells you when the internet connection drops.
- Model canvas UI improvements.

### Fixed

- The 3D viewer no longer stays blank on first launch.
- Typing in text fields works again.
- Sketch snapping points no longer drift on polygons and paths.
- Cutting a sketch on a top surface works.
- Code editor terminal error resolved.
- STL files are named from the model's parameters.

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
