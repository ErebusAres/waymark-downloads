# Waymark downloads

Windows previews for the AION 2 exploration companion.

## Install

Open [Releases](https://github.com/ErebusAres/waymark-downloads/releases), download **Waymark-0.2.5-Setup.exe**, and run it once. The tracking worker is included. No Python, GitHub CLI, GitHub account or separate updater is needed. Users on 0.2.4 should run Setup once to enable future in-app updates.

Updates show a percentage bar, then **Install and restart** installs the signed release and reopens Waymark. Settings includes check-on-launch (on by default), automatic downloading and automatic installation (both off by default). A local recovery snapshot is saved before installation. The portable ZIP remains available for manual use.

Includes terrain maps for Verteron, Altgard and Abyss; feather/gathering references; visual position tracking; minimap; character/server-pet profiles; custom pins and saved routes. This is an early preview. Most completion tracking is manual and resource availability is not live.

Shift-click adds a named pin. Ctrl-click sets a route start. Ctrl+Shift+G unlocks click-through overlays. Existing user data stays under `%LOCALAPPDATA%/AionCompanion`, separately from the app.

Each release includes a SHA-256 checksum, manifest and source revision. Npcap is installed separately for the optional passive login/pet reader; it is not bundled. The installer handles WebView2 if missing. Update signatures verify Waymark releases; a Windows publisher certificate is not configured, so Windows may display its usual reputation prompt.

The source repository is managed separately. Game artwork and third-party notices remain included in the app.
