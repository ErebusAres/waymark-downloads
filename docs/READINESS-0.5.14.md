# 0.5.14 readiness pass

| Priority | Implemented and checked offline | Still needs live evidence |
| --- | --- | --- |
| Reader reliability | Bounded partial-stream recovery; fresh identity requirement; framing-loss invalidation; transactional progress rejection; watchdog/restart tests | Launch after world entry and verify recovery from a fresh self record on the current client; continuity during real farming |
| Collection accuracy | 7-axis/category coverage display; separate permanent/reset/reward model; saved trace replays restore 372 then 11 new mapped objectives; identity isolation/duplicate/rollback tests | Installed-app trace pickup; controlled dungeon and stronghold before/clear/reward/reset scenarios. Automatic instance decoders remain disabled |
| Farming guidance | Mapped-reference/general-area distinction; optional session labels; 20 archived sessions per character; observed-rate comparison and backup preservation | Player-confirmed farming rates and actual spawn/altitude verification. No farm is labeled player-verified without that evidence |
| Map readability | Shared hover/keyboard focus; selected creature remains highlighted; matching portraits, points and patches; clearing returns normal opacity; same compact minimap renderer | Optional personal review during normal play |
| Release readiness | Packaged worker in disposable data directory; default update checks; persistence; minimap hidden/locked settings; backup/update preparation/restore; native recovery unit tests; signed installer verification | Native clean installation on a second Windows PC, including WebView2/Npcap setup |

No capture is started by release-readiness.py or the --self-test-reader command. Qualification uses synthetic data, never the live user database. Existing private recordings are replayed only into separate local copies and an in-memory database.

## Short live verification sequence

1. With a character already in the world, start Waymark. Confirm whether a fresh self identity arrives; if it does not, enter through Character Selection once. Check that an old selected profile is never presented as a current detection.
2. Collect one trace while the reader shows the correct character; verify its collection mark updates without opening the game map.
3. For one dungeon and one stronghold, retain separate before/after clear and reward observations. A later reset check must identify the actual period. Do not infer reset rewards from a first-clear checkmark.
4. On another PC, install the published build, finish setup with minimap disabled, restart and update it, then verify the minimap stays hidden and settings/pins/routes survive.

Recorded framing regression also checks ordinary skipped bytes: both saved login scenarios retain their expected trace-candidate, identity and pet-progress observations without an added identity invalidation. Explicit bounded framing recovery is tested separately from ordinary skipped message bytes.
