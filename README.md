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

### Toolbox 0.11.0 — August 18, 2026

#### New Features
**Duplicate**
- Added **Inside the folder**: *mirror the originals* (default) keeps the copies in the same sub-folders as the originals, measured from the folder they share, with the selected comp at the top; *flat* puts every copy in the one folder; *sorted by the template* files them the way the template files a fresh project. Hidden under *next to originals*, where there is no folder to arrange.

**Organize · Sort disk**
- The folder structure, your own rules, folder naming and special folders can be opened and edited from inside the Organize sheet (**Folders & rules**), and the disk structure from inside Sort disk (**Directories & rules**). Edits are live and change the plan on the same screen. Settings still holds both.

#### Improvements
- **Duplicate** and **Import** now pre-select *selected folder* whenever something is selected; *template folders* only when nothing is selected and the project has been organized; otherwise *project root*.
- **Sort disk** and **Gather** count files everywhere — the button, the list, the notes, the confirmation card and the report after — with an image sequence counted by its frames and a file shared by several items counted once. Previously the same press could show four different numbers.
- The disk confirmation card now shows the plan's warnings and "left alone" lines, and says "about" when a total includes a sequence sized by estimate.
- **Organize**'s "What to organize" rows show how many items of each kind will move, with a dimmed *n left alone* when protected or special-folder items are held back.
- **Update assets** rows read `shot_040 v01 → v02` instead of a directory on one side and a frame filename on the other.
- After an instant tool runs (Empty folders, Unused, Reduce, Consolidate, Number comps), its result line shows while the pointer is still on the tile. Previously it never appeared.
- A text field that commits when it loses focus no longer swallows the first press on the button beside it. Same fix in Import (Scan after pasting a path), Rename, Comp settings, Resize and Settings.

#### Bug Fixes
- **Import** filed footage under `mov` when the template said `01_mov` — folder numbering was ignored. Same fix for the renders folder written after a render, which created a second, unnumbered `mov` folder.
- **Duplicate** copied only the top comp when "Levels deep to copy" was cleared; blank now means the whole tree.
- **Rename** forgot seven of its options every time the panel reloaded: the four "Applies to" switches, *Fix characters that break render paths*, *Collapse double spaces* and *Strip version words*.
- **Collect** could price an image sequence at twice its size when another run shared its directory, and drop it under the size limit. Sequences are now sized from the run the plan lists.
- **Collect** flattened sub-folders on projects whose `.aep` lived in `ae/`, `aeps/` or `projects/`, or under a project-root override.
- A "located under…" rule matched in Organize but not in Import or Collect when After Effects recorded the path under `/Volumes/<boot disk>/`.
- **Render** showed only the first blocker in its footer when there were two.
- Copy from master's source picker forgot its choice on any redraw.
- Various internal fixes.

---

## Version history

| Version |  |
| :---- | :---- |
| **0.11.0** | Duplicate keeps sub-folders; the structure edits from Organize and Sort disk; disk counts are files. |
| **0.10.0** | Import's Tree view is a tree; folders tick. |
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
