# Waymark 0.5.16

- Website sync now batches changes after two minutes of quiet instead of uploading every 30 seconds. Automatic uploads are at least five minutes apart. Continuous farming gets a checkpoint after 15 minutes of pending activity.
- No new upload is triggered by unchanged progress, repeat observation timestamps, usage-clock ticks or a launch counter alone. Full current usage totals are included with the next progress/settings upload or manual Sync now; local tracking continues normally.
- Sync now bypasses the desktop activity wait. The website keeps a 30-second manual request floor to prevent repeated clicks from producing duplicate write batches.
- Failed requests retain pending progress and use backoff. A website deferral does not mark pending data as synced.
- This release includes desktop-side batching. Additional website-side write coalescing is a separate deployment, so older app versions should still update to receive the reduced upload schedule.

These intervals reduce sync requests and writes; they do not guarantee a particular D1 quota usage across all website traffic. Character pages can lag behind gameplay while changes are being batched. Saved local progress remains the authoritative copy.
