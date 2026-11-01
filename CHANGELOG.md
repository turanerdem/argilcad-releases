<div align="right">

🇹🇷 [Türkçe](CHANGELOG.tr.md)

</div>

# Changelog

All notable changes to ArgilCAD will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.11] - 2026-11-01

Technical drawings, models from photos, and a Studio camera that knows
where to look.

### Added

- **Technical drawings.** The toolbar's Drawing button opens a full drawing
  editor in five styles — Classic (ISO), Blueprint, Whiteprint, CAD night and
  Pencil on vellum. Sheets, views (sections and exploded views included),
  automatic dimensions that follow the model when it changes, holes called
  out with their counterbore, countersink or depth, a title block and a bill
  of materials. ISO by default, ASME in the US. Export to PDF, SVG and DXF.
  Drawing is free; an **AI check** of the dimensions comes with Starter and
  Pro.
- **Models from photos** (Starter and Pro). Photograph your tools on a sheet
  of A4 or Letter paper, or beside a bank card, and get a Gridfinity bin or a
  drawer insert with a pocket for each one. Or photograph a broken part, add
  a few caliper values, and get a parametric copy. The photo is measured on
  your device; dimensions nobody gave are asked for, with an estimate, and
  standard parts come from a sourced catalogue.
- **Delete my account** in Profile, with a clear list of what goes and what
  stays.
- **The Studio film's camera** can be planned from the code: say what each
  moment should show, and the camera frames it for 16:9, 1:1 and 9:16 alike.
- **Camera while playing** in Motion: frame the whole motion, follow a part,
  hold still, or play the film's camera — and orbit or zoom while it plays.
- Close the side panel per mode (⌘B, or drag the splitter) for more room.
- The modelling card can be dragged anywhere and pinned.
- AI assistants: photo tools (*list*, *get*, *add*, *measure photo*,
  *make shadow board*), *lookup standard*, *preview film*, and *open print
  section* / *get print status* for handing a model to your slicer.

### Changed

- New icons across the toolbar, the modelling tools and the mode switch.
- Tool hints show briefly while a tool is new to the project; ⓘ brings them
  back.
- Drawing and export give a clear notice when there is no model yet.
- Web: tablets can turn on full modelling (experimental, Settings › Full
  mode), and pens and fingers work in the viewer — palm rejection, no stray
  orbit from a pen tip.
- The toolbar scrolls sideways when the window is narrow.

### Fixed

- Animation play and stop.
- Draft changes being lost.
- 3D print fixes with AI.
- The example previewer.

## [1.0.10] - 2026-10-22

Real materials, a measuring tool, and a 3D print hand-off that splits,
checks and explains your print.

### Added

- **Material library.** 48 materials in the Studio — metals, plastics and
  filaments, wood, glass, rubber and more — each with its own colour palette
  (filament colours, RAL, anodised, wood species) and real surface patterns.
  Search, recent materials, previews drawn under your current lighting, and
  fine adjustments.
- **Measure.** One smart tool, in the workspace and in the Studio: point at
  an edge, circle, face or corner to read it, pick two to get the distance,
  gap, centre-to-centre or angle between them, and pin the dimension where
  you want it. Pinned dimensions follow their parts as they move, and can be
  shown in photos and videos.
- **Colours, materials, joints and animation from the code.** A model can
  carry its own look and motion — the AI now adds them on its own when they
  fit (switch it off in Settings) — and anything that moves over time, from
  an engine to a solar system, plays in the Studio.
- **3D print, much further:**
  - parts that do not fit together go onto several plates, one file each
    (a .zip in the browser);
  - a part too big for any plate is cut into pieces with alignment pins;
  - a print check names thin walls, small holes, tight clearances and
    faces printed over air, and shows them on the model;
  - supports and a brim are switched on in the file only for the parts that
    need them;
  - an **assembly booklet** shows which piece goes where;
  - together or side by side is suggested from the model itself;
  - leave out the parts you buy rather than print; one colour per plate for
    single-filament printers; filament and time estimates.
- **Fix with AI** on the print check's findings.
- AI assistants: new *set appearance*, *render photo* and *record video*
  tools, and *prepare print* takes your print settings.

### Changed

- The in-app AI now knows the Studio's materials, motion and 3D print, and
  your printer and nozzle when a request is about printing.
- **Use your own AI** is now two simple steps: copy the request, paste the
  answer back and build it. Code pasted into the prompt box runs, and an
  existing model can be changed the same way.
- Large models lay out on the print plate much faster, and the 3D print
  section shows what it is still working on.
- Support address: support@argildesign.com.

### Fixed

- Clear-coated materials and glass rendered black in high-quality renders on
  Mac.
- The 3D print section could stay on "Laying it out…" for a long time on a
  large model.

## [1.0.9] - 2026-10-15

Send your model to your slicer, see your conversation with the AI, and keep
your work backed up even without an account.

### Added

- **3D print → your slicer.** Studio's 3D print section lays the model on
  your printer's bed (automatic orientation, or the face you pick; several
  parts together or side by side) and opens a ready 3MF in Bambu Studio,
  OrcaSlicer, Creality Print or PrusaSlicer, each part on its own filament.
  Your slicer keeps its own printer, filament and quality profiles. In the
  browser the file is downloaded.
- **Conversation history** in the prompt box: every prompt in the project
  and what came of it, with a button to go back to that version, view its
  code or reuse the prompt.
- **Look & fix** (optional, in the prompt box): after building the model the
  AI looks at it from three sides and fixes what it finds, up to two rounds.
  Better models, at about 3–5× the credits.
- **Guest backups.** Without an account your projects are now backed up too
  (up to 2), in a guest session on this device. Registering keeps them;
  signing in to an existing account moves them into it. A guest session not
  used for 90 days is deleted.
- AI assistants: a new *show in ArgilCAD* tool brings the app to the front,
  and *prepare print* hands the print layout to your assistant.

### Changed

- New AI models: Claude Haiku 5.5 (default), Sonnet 5.5 and Opus 5.5 (Pro),
  GPT-6.1 Sol and GPT-6 Luna. GPT-5.5 is no longer offered; if you had
  picked it, choose another model.
- Prompt-to-model now follows the real product's form and function more
  closely, and fasteners, bearings and gears are built with valid sizes.
- AI assistants look at their own model and fix it before finishing, and
  their screenshots work while ArgilCAD is behind other windows or
  minimised.

### Fixed

- Windows: a computer without the WebView2 Runtime now says so, with a
  download button, instead of an empty 3D view; the installer warns when it
  cannot install the runtime.
- Windows: a damaged system font no longer stops the modelling engine from
  starting.
- An Intel Mac now says the desktop app needs Apple Silicon and offers the
  browser version, instead of a generic setup error.
- A description over 2000 characters (600 for a change) is refused with a
  clear message before any credit is spent.
- An error after cancelling a modelling tool mid-run no longer goes unshown.
- Clearer edges in the 3D view.

## [1.0.8] - 2026-10-06

Bring your own AI assistant to ArgilCAD.

### Added

- **AI assistants (Starter and Pro).** Claude Desktop, Claude Code, Codex,
  Gemini CLI, Cursor, VS Code and other MCP clients can now design parts in
  ArgilCAD on your own AI subscription. Your assistant builds the model in
  your project, looks at it, fixes what is off and exports STEP, STL or 3MF.
  Every step lands in your timeline, where you can undo it, and work done
  this way uses no ArgilCAD credits.
- **AI assistant button** in the top bar: one click turns it on, and it turns
  green once your AI client is connected. Settings → AI assistants shows how
  to set up each client, and an illustrated guide is at
  [argildesign.com/products/argilcad/connect.html](https://argildesign.com/products/argilcad/connect.html).
- Your assistant opens or creates a project by itself when none is open.

### Notes

- In the browser, the AI assistant connects from every major browser except
  Safari. In Safari, use the desktop app.

## [1.0.7] - 2026-09-29

A new Studio mode dresses your model, renders it and sets it in motion, and
models made of several parts can now be worked on part by part.

### Added

- **Studio mode**, beside Workspace and Explore, with its own buttons in the
  viewer's toolbar: Material, 3D print, Motion, Photo and Video.
- **Materials and lighting.** Give each part its own material and colour. The
  look is saved with the project and travels with its backup.
- **3D print preview.** See layer lines on your model, on a build plate at
  real scale.
- **Coloured 3MF.** Once a project is dressed, its 3MF export carries each
  part's colour to your slicer.
- **Photos and renders.** Save a PNG snapshot of the view. Starter and Pro
  add studio lighting (HDRI) and a path-traced render — up to 2K on Starter
  and 4K on Pro.
- **Motion.** Explode an assembly and put it back together. Hinges, sliders
  and gear trains are suggested from the model's geometry, and you drag the
  moving parts on the model itself. Parts that run into each other while they
  move are shown in red.
- **Video.** Record the motion as an MP4: 720p with a small ArgilCAD mark on
  the free plan, 1080p on Starter, 4K on Pro.
- **Models with several parts.** A new Parts explorer lists each part, with
  its features under it. Hide, isolate or highlight a part; rename, join or
  remove one; export or draw a single part; start a sketch as a new part.
  The modelling tools work on the part you picked, and a part keeps its
  number until you rename it.
- **AI that knows about parts and motion.** Ask for a hinged lid, a gear pair
  or a drawer, and the generated model comes as separate parts that Studio
  can set in motion.

### Changed

- **Sketching on a face.** The plane previews its grid before you click, a
  dot follows the pointer with its distances, the grid runs along the face's
  edges, and you can type the next point's distance to an edge.
- The code editor's line numbers and the timeline's rows fit narrow panes
  without overflowing.
- Panel dividers show a grip, so they read as something to drag.

### Fixed

- Clear Model now empties the viewer, and the next model is framed as a new
  one.
- Switching projects no longer carries the previous project's selection,
  measurements, tools or step plan into the next one.

## [1.0.6] - 2026-09-21

ArgilCAD now opens on phones and tablets, showing the models you keep in your
account. Building, editing and generating stay on a computer, where the CAD
engine runs.

### Added

- **ArgilCAD on phones and tablets.** Open
  [argildesign.com/argilcad](https://argildesign.com/argilcad/) on a handheld
  and it shows your models, with a bottom bar for moving between the code and
  the model. Editing and new models stay on a computer.
- **Models on your devices** (Starter and Pro). Mark a project and its
  finished model is kept in your account, so your phone and tablet can show
  it — 2 models on Starter, 10 on Pro, and you choose which ones, month to
  month.
- **Your work comes back.** Project sync now reads your account as well as
  writing to it: open a project and it shows the version you last worked on
  elsewhere. Edited in two places, you are asked which one stands — nothing is
  overwritten behind your back.
- **The viewer follows the editor.** Code arriving from another device is run
  where there is an engine to run it, so the model on screen matches the code
  beside it.
- **Examples on a handheld.** Explore's examples come ready-built, so a phone
  can open them with no CAD engine of its own.

### Changed

- The top bar shows how many of your model slots are in use, with the month's
  remaining allowance in its tooltip.
- Model sync and project backup are named apart now: the backup keeps your
  projects' code, sync keeps their models.
- The local CAD backend no longer draws itself with a cloud icon — it is a
  process on your own machine.

### Fixed

- Opening a synced project on a phone no longer hangs the app.
- A project built by writing code and pressing Run is now found by sync. It
  used to answer "run this project once first" however many times you had run
  it.
- A failed rebuild no longer erases the model that had just been downloaded.
- A synced model that becomes available after a project opens is now fetched,
  instead of leaving the viewer empty.
- Synced models download in the browser at all now — the storage bucket had no
  CORS configuration, so every fetch was refused.
- Phones and tablets can reach the web app from the marketing site, instead of
  the link being handed to the share sheet.

## [1.0.5] - 2026-09-14

ArgilCAD now runs in your browser too, and AI generation moves to the Starter
and Pro plans. Everything that runs on your own machine — the code editor, the
modelling tools, examples, exports and drawings — stays free, with no account
needed.

### Added

- **ArgilCAD in the browser** at
  [argildesign.com/argilcad](https://argildesign.com/argilcad/): the same app,
  with models built on your own device.
- **Project backups.** When you are signed in, your projects' code is kept in
  your account and opens on your other devices, the browser included. Turn it
  off in Profile; deleting a project deletes its backup.
- **Examples in the prompt box.** Without a plan, three ready-made examples
  (Spur Gear, Vase, Electronics Enclosure) build on your machine at no cost,
  beside a way to prompt your own AI and paste the code back.
- **Generate leads to what you need.** Pressing Generate without a plan opens
  sign-up, then the plans, and your prompt stays where it was. Once a plan is
  active, generating is one tap away.
- **A heads-up before Starter credits run out**, at 80% and 100% of the month's
  allowance, with an in-place upgrade to Pro.
- **The prompt box folds away** to a small pill (Esc in an empty box, or
  View › Prompt box); press **P** to bring it back.

### Changed

- **AI generation takes a Starter or Pro plan.** The free monthly and trial
  credits have ended; credits you already have stay usable until they are
  spent.
- **No account needed to start.** The app opens without creating one; sign up
  when you want a plan or your projects in your account.
- **Usage analytics only with your permission.** Nothing is sent until you
  answer the prompt on first launch, and you can change your answer in
  Settings.
- The CAD engine's versions are pinned, so the desktop app and the browser
  build identical models.
- The Privacy Policy and Terms of Service were updated (effective September 14,
  2026).

### Fixed

- The first modelling tool applied to an unchanged example no longer fails
  with a `NameError`.
- Exporting or drawing a model reopened from history works again after the
  built-in engine has restarted.
- Small or short windows no longer cut off the top bar, panels and dialogs.

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
