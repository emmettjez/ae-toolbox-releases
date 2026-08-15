# Toolbox for After Effects

Toolbox is a suite of project and file management tools for After Effects.

### ⬇ [Download Toolbox](https://github.com/emmettjez/ae-toolbox-releases/releases/latest/download/ae-toolbox-latest.pkg)

It installs as a dockable panel: **Window › Extensions › Toolbox**.

Once installed, Toolbox tells you when a new version is available and updates itself — you should only need to download it once.

Toolbox is organized into three modules:

---

## Project — clean up and reorganize the project itself

### Folders & files

| Tool | What it does |
| :---- | :---- |
| **Organize** | Files every comp and asset into a folder structure you define or pick from a template. |
| **Sort disk** | Organize the project’s files on disk into a structure you define or pick from a template. |
| **Gather** | Finds footage living outside your project directory and moves it in, so the job is self-contained. |
| **Relink** | Searches for missing footage across directories and reconnects it. |
| **Collect** | Copies the project and its footage, including proxies, to one destination. Whole project, or reduced to chosen comps. |
| **Empty** | Remove empty folders from your After Effects project. |

### Names

| Tool | What it does |
| :---- | :---- |
| **Rename** | Bulk renaming — find and replace, prefixes and suffixes, numbering. |
| **Number** | Numbers your comps by tier, so the numbering reflects the actual structure instead of the order you happened to build things in. |

### Fixes

| Tool | What it does |
| :---- | :---- |
| **Comp settings** | Sets frame rate, dimensions and duration across many comps. |
| **Resize** | Changes a comp's resolution — with its precomps, text, masks, lights, cameras and effects — so the render is identical at the new size. |

### Remove

| Tool | What it does |
| :---- | :---- |
| **Unused** | Deletes comps, footage and solids that nothing references. |
| **Reduce** | Removes items not used by the chosen comps. Expression references count as use. |
| **Consolidate** | Cleans up after importing another .aep: links the imported items to files you already have and removes the duplicates. |

### Create

| Tool | What it does |
| :---- | :---- |
| **Duplicate** | Duplicates a comp *and* its precomp tree, rewired to the copies — not left sharing the originals. Expression and effect aware. |

---

## Render — easier render management, including background render

| Feature | What it does |
| :---- | :---- |
| **Naming** | Builds output filenames from comp names: find and replace, added text, tokens. |
| **Output** | Pick from recent and saved locations, and save into automatically named folders. |
| **Versioning** | Reads existing version numbers on disk and in the render queue, and uses the next. |
| **Background rendering** | Renders in a separate After Effects instance. Finished renders are imported on request. |

---

## Import — bring in footage and keep it current

| Tool | What it does |
| :---- | :---- |
| **Import assets** | Browses directories and imports footage, stills and image sequences. |
| **Update assets** | Looks for new versions of assets in your project and updates them. |

---

## What's new in this version

### Toolbox 0.8.3 — August 14, 2026

#### New Features

**Collect**
- Added a scope option: collect the whole project, or only chosen comps.
- Footage and comp proxies are collected and relinked. Missing proxy files are reported.
- Gather can include image sequences (off by default). Sequences are copied whole; incomplete runs are reported.

#### Improvements

**Collect**
- The file-type exclusion list starts empty and lists only types present in the project. Exclusions do not persist between sessions.
- A separate expression scan is no longer required.

#### Bug Fixes

- Fixed layered Photoshop and Illustrator items collecting as the flattened document. Same fix in Sort disk, Relink, and Gather.
- Fixed Sort disk skipping image sequences with the sequence option enabled.

## Version history

| Version |  |
| :---- | :---- |
| **0.8.3** | Collect: whole-project scope, proxies, image sequences. |
| **0.8.2** | Resize. |
| **0.8.1** | Fixes and improvements. |
| **0.8.0** | Update notifications, shown in the panel header. |
| **0.7.1 – 0.7.4** | Fixes and refinements to updating and installing. |
| **0.7.0** | First public release, and the first that can update itself. |

Full notes for every release are on the [Releases page](https://github.com/emmettjez/ae-toolbox-releases/releases).

---

## Install

1. Download [`ae-toolbox-latest.pkg`](https://github.com/emmettjez/ae-toolbox-releases/releases/latest/download/ae-toolbox-latest.pkg) — always the newest version.  
2. **Double-click it** and follow the installer. It asks for no password and installs only into your own user folder.  
3. **Quit After Effects completely and reopen it** — extensions are only scanned at launch.  
4. Open it from **Window › Extensions › Toolbox**.

The installer is signed, and notarized by Apple, so macOS opens it without a warning.

**Prefer to place the files yourself?** Every release also carries a `.zip` with the extension folder and an `INSTALL.md`. macOS blocks the `Install.command` inside it with a “cannot be verified” warning — the `.pkg` above exists to avoid that.

## Updating

**Toolbox updates itself inside After Effects.** It checks for new releases once a day, shortly after the panel opens, and shows a notice in the panel when something new is available — one button installs it, and you restart After Effects to pick it up. From Settings you can check at any moment, or change how often the automatic check runs: every time the panel opens, daily, weekly, or never.

It keeps the previous version alongside the new one, so a build that misbehaves can be put back. This is the only thing Toolbox uses the network for.

## Your files

Templates, preferences and saved locations live in `~/Library/Application Support/Toolbox/` and are never touched by an install or an update.

## Requirements

**macOS.** There is no Windows version.

Toolbox does not restrict which After Effects version it runs in.
