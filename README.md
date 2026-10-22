# Waymark for AION 2

**Maps, farming routes and pet progress for AION 2.**

Waymark is a Windows app for AION 2 Global Steam. Explore the world map, build farming routes, and follow your pet collection in one place. A floating minimap keeps nearby objectives visible while you play.

[**Download Waymark 0.3.6 for Windows**](https://github.com/ErebusAres/waymark-downloads/releases/download/v0.3.6/Waymark-0.3.6-Setup.exe) · [Getting started](docs/GETTING_STARTED.md) · [Release notes](https://github.com/ErebusAres/waymark-downloads/releases/tag/v0.3.6) · [All downloads](https://github.com/ErebusAres/waymark-downloads/releases)

Windows 10/11, 64-bit. Public preview. No GitHub account needed to download.

![Waymark exploration map with terrain, map layers and a glowing player marker](docs/images/explore.jpg)

## Explore with a purpose

- **World maps with terrain.** Find feathers, gathering nodes, kibelisks, sealed dungeons and strongholds. Verteron and Altgard use English kibelisk names; Abyss reference maps are also included.
- **Choose what appears.** Toggle whole categories, resource groups or individual resources. Show every enabled marker when zoomed out, or turn on grouping.
- **Keep your own routes.** Name custom pins, choose a route start and save a circuit. Filters, follow mode, routes and map views are remembered.
- **A minimap that fits your setup.** Move it, cycle three zoom levels, or scroll to zoom while unlocked. It stays above other windows and can lock with click-through enabled.
- **Choose your own colors.** Personalize the player marker and glow, pet ranks and map accents in Settings → Appearance. Reset one color or restore the original palette.
- **Track collection progress.** Mark individual objectives or declare a whole category complete for a character. Progress can be reset in Settings.

## See your next pet upgrade

Pet cards bring together portraits, names, farming locations, levels and soul progress. Closest to complete is the default order, with completed level 3 pets at the bottom. Switch to alphabetical, least progress first, or recent pickups.

Missing starting levels use clearly labeled estimates from zero. Pickups advance those estimates at 5, 25 and 75 souls; confirmed game readings replace them. Estimated maximum ranks remain visible for farming. Supported live soul pickups update progress without relogging, and reaching a tier threshold advances the displayed level. If a level is missing or appears stale, open that pet’s in-game card with the game focused for a few seconds. Waymark checks the selected tile against the card and updates the saved rank and count automatically. Card verification currently supports the English pet screen and uses Windows’ built-in OCR. Pet progress is shared between characters on the same server. Farming locations use reference monster spawn points where available, with regional fallbacks labeled separately.

![Waymark pet page with compact cards and soul progress bars](docs/images/pets.jpg)

*Screenshots use an example profile and illustrative progress.*

## A cleaner desktop workspace

The 0.3.0 refresh gives maps and pet cards more room, keeps controls consistent, and separates everyday settings from capture and calibration tools. Settings now has General, Appearance, Updates, Data & backups, Connection and Advanced sections.

![Waymark settings with a dedicated navigation list](docs/images/settings.jpg)

## Start playing

1. Download and run **Waymark-0.3.6-Setup.exe**. Setup includes the WebView2 bootstrapper if the Windows web runtime is missing.
2. Choose a starting map and whether to open the floating minimap. You can change both later.
3. For automatic character and pet reads, install [Npcap from its official site](https://npcap.com/#download) with **WinPcap API-compatible Mode** enabled. Map planning works without it.
4. Start Waymark before entering your character. If you opened Waymark while already in game, return to character selection and enter once so it can identify the session.
5. Open the in-game map briefly to acquire a visual position, then choose your layers and route.

See the [getting-started guide](docs/GETTING_STARTED.md) for controls, update settings, troubleshooting and backups.

## Current coverage

Waymark is under active development. Visual position tracking is verified in Verteron and Altgard. Abyss tracking and cross-faction transitions still need live validation. Position comes from visible game terrain; a last-known marker remains visible when a fresh fix is unavailable.

Resource and pet spawn markers are reference locations, not a live spawn-availability feed. Routes connect map objectives; they do not calculate a walkable path around terrain. Automatic claimed-feather recognition is limited to supported Verteron map views. Dungeon and stronghold completion, including reset-period rewards, is not yet fully detected automatically; use manual collection controls where needed. Inventory and other character information depend on the fields the reader can currently observe.

## Updates and local data

Waymark checks for updates on launch by default. Download and automatic installation preferences are available in **Settings → Updates**. Downloads show progress; installing an update restarts the app. The built-in updater verifies release signatures before installation.

Character observations, progress, pins, routes and settings are stored locally. Waymark does not ask for your game password, control your character or inject code into the game. Research recordings are explicit local captures, not automatic uploads. Use **Settings → Data & backups** before moving or resetting data.

## Help and feedback

[Report a problem or request a feature](https://github.com/ErebusAres/waymark-downloads/issues). Include the Waymark version, map, steps to reproduce and a screenshot if useful. Settings → Connection can review/copy or save a diagnostic report with status codes and counts, excluding names, IDs, locations, paths and packet data. See [detection coverage](docs/DETECTION_COVERAGE.md). Keep login details and packet captures out of public issues.

This repository contains public downloads and documentation. Application source is maintained separately. Waymark is an independent project and is not affiliated with NCSOFT. AION 2 names and game artwork belong to their respective owners; bundled attribution accompanies the app.
