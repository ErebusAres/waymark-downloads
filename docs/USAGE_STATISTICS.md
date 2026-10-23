# Usage statistics

Basic usage counters are collected automatically and stored in the local SQLite database. Settings > Statistics shows this installation’s totals, with a counts-only summary and reporting JSON export. No reporting service is configured yet, so the current implementation makes no statistics upload. The future site can ingest the cumulative report format without an opt-in flow.

## Definitions

- Characters seen: distinct verified Global/server/character-name identities observed after tracking starts. Repeated logins and character swaps do not repeat a known identity. Names are normalized with Unicode NFC before hashing; a rename or server move can establish a new identity. This is not a count of people or game accounts.
- App session time: cumulative native application time, including background/minimap use. The Windows unbiased interrupt clock excludes system sleep. A native timer checkpoints cumulative elapsed seconds every 30 seconds independently of WebView focus and records a final pulse on normal main-window close. An abrupt exit or update handoff can lose the final uncommitted interval. Multiple native app processes are separate sessions; minimap windows do not create sessions.
- Connected time: intervals between committed reader status pulses with the same verified reader session and detected character. Pauses, replacements and gaps longer than five seconds do not add time.
- Souls observed: amounts from accepted live pickup events, after existing identity, timestamp and sequence deduplication. Login totals, historical captures and estimated progress are not backfilled into the counter.
- Rank-ups tracked: distinct observed pet/tier transitions from a known starting rank, including threshold advancement from verified baselines. Repeated equal-rank messages and estimated ranks do not count. Each region/server/pet/tier is counted at most once per installation, including after a game-progress restore.
- Pets leveled: distinct server-shared pets with at least one such tracked transition. Pets maxed: distinct pets with a tracked transition to Lv.3. Initial observations of an already maxed pet do not add an achievement.
- App launches: distinct native application sessions. Reader restarts and extra windows do not add launches.

Counters begin when this version first records activity. Existing history is not reconstructed. Metrics and accepted game observations commit in the same transaction. A failed metrics write rolls back only its savepoint, preserving the core observation. A private backup of the complete database includes statistics. Portable game-state backups do not export or reset installation statistics; those remain on this PC.

## Future combined reporting

`WaymarkUsageReport` version 1 contains an installation UUID, tracking start time, report time, cumulative counters and deterministic SHA-256 character-identity keys under a versioned namespace. It excludes raw character names, server labels, positions, inventory, chat and packet data. These keys are pseudonymous identifiers, not a guarantee of anonymity. The public copied summary contains counts only.

A reporting backend must upsert the high-water counters for each installation, never sum every received snapshot. Character keys are unioned across installations for deduplication; `usage_metrics.combine_reports` implements and tests these rollup semantics. Installs are not people, and separate fresh installations can contribute separate app-time and pet-event counters. No account linkage or cross-account pet identity is inferred.

A future ingestion service still needs a configured endpoint, storage, rate limits, retention and published public-summary rules. Exported reports are ready for that service; there is no fabricated global total or hidden fallback destination in the current build.
