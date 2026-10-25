# Waymark 0.5.14

- Hover or keyboard-focus a creature’s spawn marker to highlight matching portraits, reference points and patches. Selecting it keeps the focus; dismiss the location to show all creatures normally. Other map categories remain visible.
- Add an optional farming-session label and compare the last 20 completed sessions for each character. Starting a new session archives the previous active one. History and labels are local and included in full backups. Rates count observed pickups and connected farming time.
- Pet location details distinguish mapped spawn references from general areas. A source check is not a player-verified farming rate.
- The reader can recover framing from a partial connection using bounded validated-bundle checks. It still requires a fresh self-identity message; attaching to every already logged-in session is not yet verified. Lost framing or a character-change snapshot clears stale identity.
- Invalid progress observations roll back independently and no longer restart capture. Connection diagnostics show rejected-observation counts and separate completion support for collections, first clears, reset-period clears and rewards.
- Fresh-data qualification checks saved settings, pins/routes, minimap visibility, pre-update backups and restoration. A synthetic packaged-reader self-test exercises framing and login decoding without starting capture or writing player state.

Automatic dungeon/stronghold decoding remains unavailable. Recorded trace regression passed without changing live progress; current-game cold attachment and installed-app trace pickup still need controlled live verification. A clean native installation on a second PC remains a separate check.
