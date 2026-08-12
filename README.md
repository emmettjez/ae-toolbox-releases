# Toolbox for After Effects

**Toolbox is a suite of project and file management tools for After Effects.**

It works from a real dependency graph of your project — what actually references what —
rather than guessing from filenames. It installs as a dockable panel:
**Window › Extensions › Toolbox**.

**This repository holds the builds.** The source lives in a private repository.

Toolbox is organised into three modules. It features the following tools:

---

## Project — clean up and reorganise the project itself

### Folders & files

| Tool | What it does |
|---|---|
| **Organize items into folders** | Files every comp and asset into a folder structure you define. The structure is yours — a template you can edit, save and reuse across projects. |
| **Organize files on disk** | Applies that same structure to the actual files on disk, so the project panel and the folder on your drive finally agree. |
| **Bring stray files into the project** | Finds footage living outside your project directory and moves it in, so the job is self-contained. |
| **Relink missing footage** | Searches for missing footage and reconnects it — the whole project or just what you select. Handles image sequences as sequences. |
| **Collect footage into a new directory** | A Collect Files that actually reduces: copies the project and only the footage it needs to a new directory beside it. |
| **Remove empty folders** | Clears out the empty folders left behind after a reorganise. Leaves your create-only folders alone. |

### Names

| Tool | What it does |
|---|---|
| **Rename items** | Bulk renaming — find and replace, prefixes and suffixes, numbering. Works on a selection or the whole project. |
| **Number comps by how deep they sit** | Numbers your comps by tier, so the numbering reflects the actual structure instead of the order you happened to build things in. |

### Fixes

| Tool | What it does |
|---|---|
| **Conform comp frame rates** | Brings comps onto one frame rate. |

### Remove

| Tool | What it does |
|---|---|
| **Remove unused items** | Deletes comps, footage and solids that nothing references. |
| **Reduce to masters** | Keeps your deliverables and everything they use, and removes the rest. Expression-aware, so a comp referenced only by `comp("X")` survives. |
| **Consolidate imported project** | Cleans up after importing another .aep: links the imported items to files you already have and removes the duplicates. |

### Create

| Tool | What it does |
|---|---|
| **Duplicate comp with its assets** | Duplicates a comp *and* its precomp tree, rewired to the copies — not left sharing the originals. |

---

## Render — queue renders, in the background, and bring them back

Set up outputs without hand-typing paths, then render without tying up After Effects.

| Tool | What it does |
|---|---|
| **Add** | Pick the comps to render. |
| **Preset** | Choose the output module preset. The list is read from your own machine, so it only ever offers formats that machine can actually write. |
| **Name** | Builds the output name from your comp names and tokens, so everything is named consistently instead of by hand. |
| **Output** | Where it lands, and how it is foldered. Handles versioning for you: it reads the version numbers already on disk *and* in the queue, and takes the next one — so you don't overwrite yesterday's render. |
| **After render** | Bring the finished render straight back into the project: import it, import and replace what it was made from, or set it as a proxy. |
| **Will write** | The exact paths before you commit — what is fine, what would overwrite something, and what is blocked. The path shown is the path written. |
| **How** | **Render here**, which blocks After Effects until it finishes, or **render in the background**, which hands it to a second After Effects that quits when it is done — so the one you are working in stays usable. |
| **Finished renders** | Tells you when background renders have finished, and brings them in on a press. A background render can't import into a project it isn't holding, so Toolbox does that part for it — and only into the project the render actually came from. |

---

## Import — bring in footage and keep it current

| Tool | What it does |
|---|---|
| **Import assets** | Browse or paste a path, see what's there, filter it down, and import — with image sequences detected and brought in as sequences. |
| **Update assets** | Finds newer versions of footage you've already imported and repoints your comps at them. |

---

## What's new in this version

### 0.8.1

**Fixes and improvements.**

- **Remove unused items** now leaves anything you have marked `[KEEP]` alone, and no
  longer removes comps that are used only by an expression. If you tag something to
  protect it, it stays.
- Various internal improvements and housekeeping.

### 0.8.0

**Toolbox now tells you when there's a new version.** A check runs shortly after the panel
opens, once a day. When something new is available, a strip appears under the header with
what changed and a button to install it.

- Dismissing an update stops it asking about that version. The next one speaks up again.
- A small dot stays on the gear while an update is available, so dismissing means *stop
  interrupting*, not *hide it*.
- Nothing appears when you're up to date, or when the check can't reach GitHub.

Previously the check only ran if you went looking for it in Settings.

## Version history

| Version | |
|---|---|
| **0.8.1** | Fixes and improvements. |
| **0.8.0** | Update notifications, shown in the panel header. |
| **0.7.1 – 0.7.4** | Fixes and refinements to updating and installing. |
| **0.7.0** | First public release, and the first that can update itself. |

Full notes for every release are on the
[Releases page](https://github.com/emmettjez/ae-toolbox-releases/releases).

---

## Install

1. Download `ae-toolbox-latest.zip` from
   [the latest release](https://github.com/emmettjez/ae-toolbox-releases/releases/latest).
2. Unzip it and double-click `Install.command`.
3. **Quit After Effects completely and reopen it** — extensions are only scanned at launch.
4. Open it from **Window › Extensions › Toolbox**.

Full instructions are in `INSTALL.md` inside the zip.

## Updating

**Toolbox updates itself inside After Effects.** It checks for new releases on startup and
shows a notice in the panel when one is available — one button installs it, and you restart
After Effects to pick it up. You can also check any time from Settings (the gear).

It keeps the previous version alongside the new one, so a build that misbehaves can be put
back. This is the only thing Toolbox uses the network for.

You should only need to install by hand once.

## Your files

Templates, preferences and saved locations live in
`~/Library/Application Support/Toolbox/` and are never touched by an install or an update.

## Requirements

**macOS.** The zip ships `Install.command` and nothing else — there is no Windows installer.

Toolbox does not restrict which After Effects version it runs in. It is built and used
daily in **2026**, and installed alongside 2024 and 2025.

## Trust

These builds are **unsigned**, so installing one requires enabling Adobe's
`PlayerDebugMode` — which also permits any *other* unsigned extension on that machine. The
installer does this and prints how to undo it.

The panel runs with Node access: it reads and writes files as you, which is what lets it
move footage, collect projects and render. It talks to the network for exactly one purpose
— checking this repository's releases.
