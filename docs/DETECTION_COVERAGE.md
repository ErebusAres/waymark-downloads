# Current detection coverage

This page is the current product boundary. Older feasibility, validation and reuse notes describe dated implementation stages, not current setup instructions.

| Area | Available now | Remaining limit |
| --- | --- | --- |
| Player location | Local visual terrain matching, glowing live/last-known dot | Needs visible supported game terrain; continuous movement, custom HUDs, interiors and real Abyss/Timespace transitions are not fully validated. No production packet-coordinate decoder. |
| Character | Passive Global Steam login identity and profile switching | Partial-stream framing recovery is available, but a fresh self-identity message is still required. Starting before world entry remains the reliable path; current-client mid-session recovery needs live verification. A saved profile is not proof of the current character. |
| Pets | Server-shared observations, live supported soul gains, tier progress, farming summary, selected-card verification | Missing ranks use labeled zero-based estimates from observed pickups until verified. English selected cards can reconcile levels and counts while the game is focused; unopened cards are not scanned. Session totals include observed pickups only. Reference spawns are not live monsters or verified altitude. |
| Empyrean Traces | Character-bound achievement pickups and login restoration for reviewed Verteron, Altgard and Abyss map references; checked Verteron icons as fallback | Requires a fresh character entry after reader restart. Ambiguous/missing catalog matches are excluded. Map visibility is only needed for the visual fallback. |
| Dungeons / strongholds | Manual marks and separate first-clear/reset/reward evidence model | Automatic game decoders are not enabled. Clearing and reward claiming are distinct. No guessed reset schedule. |
| Kibelisks / cubes | Reference markers and manual planning | Automatic activation/collection tracking is not implemented. |
| Kina / Odyle / points / inventory | Manual counters and material targets | Automatic current-client inventory, resource, stat and skill readers are not enabled. |
| Maps / routes | Verteron, Altgard and Abyss reference terrain; saved routes, pins and filters | Routes are straight-line guidance, not walkable navigation. Resource availability and respawn times are not detected. |

## NotMeter

Passive character/pet reading can run alongside NotMeter using independent Npcap handles. Independent processes and filter isolation were verified with self-owned localhost traffic; simultaneous actual gameplay still needs validation. There is no NotMeter data bridge. A2Tools/AetherTrail coexistence remains blocked. Explicit research recording still requires closing the other capture apps.

## Diagnostics and data

Settings → Connection shows detailed local reader status. Review/copy or save a support report for status codes and counts without character/server IDs, names, maps, coordinates, paths, IPs, arbitrary error text or packets. Reports are never uploaded automatically. They summarize current detection; they do not recover missing observations or enable unsupported decoders.

Manual completion and game evidence stay separate. Local backups preserve profiles, server pets, history, pins, routes and preferences; raw recordings are excluded.

Connection diagnostics list collection, first-clear, reset-period clear and reward decoder coverage separately. Rejected observations are rolled back without restarting capture. Local farming-session history retains the last 20 completed sessions per character, with optional labels; it does not establish player-verified farm locations. See [0.5.14 readiness boundaries](READINESS-0.5.14.md).
