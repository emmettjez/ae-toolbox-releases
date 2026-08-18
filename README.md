# Toolbox for After Effects

Toolbox is a suite of project and file management tools for After Effects.

### ⬇ [Download Toolbox](https://github.com/emmettjez/ae-toolbox-releases/releases/latest/download/ae-toolbox-latest.pkg)

It installs as a dockable panel: **Window › Extensions › Toolbox**.

### 📖 [Read the manual](https://emmettjez.github.io/ae-toolbox-releases/)

How to set up a project, a page for every tool, and the things you might not think to do. The **?** in the panel header opens it too.

Once installed, Toolbox tells you when a new version is available and updates itself — you should only need to download it once.

Toolbox is one grid of tools, in categories laid out in the order a job runs:

---

## Import — bring in footage and keep it current

| Tool | What it does |
| :---- | :---- |
| **Import** | Browses directories and imports footage, stills and image sequences. |
| **Update** | Looks for new versions of assets in your project and updates them. |

---

## Project tools — clean up and reorganize the project itself

### Folders & files

| Tool | What it does |
| :---- | :---- |
| **Organize** | Files every comp and asset into a folder structure you define or pick from a template. |
| **Sort disk** | Organize the project’s files on disk into a structure you define or pick from a template. |
| **Gather** | Finds footage living outside your project directory and moves it in, so the job is self-contained. |
| **Relink** | Searches for missing footage across directories and reconnects it. |
| **Collect** | Copies the project and its footage, including proxies, to one destination. Whole project, or reduced to chosen comps. |

### Names

| Tool | What it does |
| :---- | :---- |
| **Rename** | Bulk renaming — find and replace, prefixes and suffixes, numbering. |
| **Number comps** | Numbers your comps by tier, so the numbering reflects the actual structure instead of the order you happened to build things in. |

### Fixes

| Tool | What it does |
| :---- | :---- |
| **Comp settings** | Sets frame rate, dimensions and duration across many comps. |
| **Resize** | Changes a comp's resolution — with its precomps, text, masks, lights, cameras and effects — so the render is identical at the new size. |
| **Versions** | Lists assets held at more than one version and can repoint every use to the newest. |
| **Missing frames** | Checks every image sequence for frames missing inside its range. |

### Remove

| Tool | What it does |
| :---- | :---- |
| **Empty folders** | Remove empty folders from your After Effects project. |
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


## What's new in this version

### Toolbox 0.9.0 — August 18, 2026

#### New Features
**Settings**
- Your own rules are cards. A card is one or more tests, all of which must hold — name, extension (one or more), kind, located under a disk folder, in a project folder, changed in the last N days or weeks — and a folder to send matches to. Cards are checked before the structure's kinds, top to bottom; the first card that matches an item takes it.
- Each card shows a live count of what it catches in the open project, and says why it is zero: matches nothing here, not finished, taken by a card above, or needs masters declared. Clicking the count lists the items.
- **+ from selection** starts a card from what the selected items share: extension, kind, a common directory, or a selected folder.
- A card using a folder or age test is re-checked every time Organize runs, so an item that has moved or aged out is filed differently on a later run.
- Settings is laid out in bands: the structure is a table with a Now column counting what the open project has of each kind, the Project panel and Disk halves switch on the band heading, and special folders are chips.

**Rename**
- The kinds a run may touch are one block, Applies to: Comps, Solids, Footage, and the names After Effects wrote itself. All four are inclusions.
- Numbering is one question — leave alone, add a counter, or restyle what's there — and each answer shows only its own rows. A lone number is a version and Close gaps in a set are options of restyling.
- Name pattern is its own band. {name} is the name after every other step, {n} the counter.

#### Improvements
- Custom rules match in the order they are listed. Previously a name rule was matched before an extension rule regardless of order.
- The Import scan reads dates and sizes in chunks after the walk, with its progress shown in the sheet, and Stop ends it. Previously the panel was unresponsive for the whole of that read, and Stop did not stop it.
- An Import scan asks each time before switching to the After Effects reader; the remembered answer applies to Relink and Update only.
- Typing in a filter or a path field no longer redraws the sheet on every keystroke.

#### Bug Fixes
- Fixed the Rename sheet drawing Comps, Solids, Fix characters and Collapse double spaces unchecked while the run treated them as on.
- Fixed rule cards and Disk edits in Settings not being saved.
- Fixed the Import scan showing no progress and Stop appearing to do nothing while a scan ran.
- Fixed the panel repainting a large Import listing on every four files while lengths were read; a listing of 137,000 rows left the panel unresponsive for minutes.
- Fixed two Settings rows overflowing at the panel's minimum width.

## Version history

| Version |  |
| :---- | :---- |
| **0.9.0** | Rule cards; Settings and Rename redesigned. |
| **0.8.5 – 0.8.6** | One grid of tools; Import and Render open as sheets. |
| **0.8.4** | Managed / Unmanaged project directory; render destination remembered per project. |
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
