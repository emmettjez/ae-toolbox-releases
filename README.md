# Toolbox — releases

Packaged builds of the After Effects **Toolbox** panel, a dockable CEP extension that
reorganises, reconciles and audits AE projects from a real dependency graph.

**This repository holds builds only.** The source lives in a private repository.

## Install

Download the newest `ae-toolbox-<version>.zip` from
[Releases](https://github.com/emmettjez/ae-toolbox-releases/releases), unzip it, and
double-click `Install.command`. Then **quit After Effects completely and reopen** —
extensions are only scanned at launch.

Open it from **Window › Extensions › Toolbox**.

Your templates, preferences and saved locations live in
`~/Library/Application Support/Toolbox/` and are never touched by an install.

## Updating

From **0.7.0** onward the panel can update itself: open Settings (the gear), press
**Check for updates**, and it will fetch the newest release from here. It stages the
download, verifies it, and keeps the previous version alongside so a bad build can be
put back.

## Trust

These builds are **unsigned**, so installing one requires enabling Adobe's
`PlayerDebugMode` — which also permits any *other* unsigned extension on that machine.
The installer does this and prints how to undo it.

The panel runs with Node access: it reads and writes files as you, which is what lets it
move footage, collect projects and render. It talks to the network for exactly one
purpose — checking this repository's releases.
