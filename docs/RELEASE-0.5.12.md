# Waymark 0.5.12

## Text size

- Open Settings > Appearance > Text size to adjust the main app and minimap independently.
- Choose 100% to 200% in 5% steps. 100% preserves the current appearance and is the smallest setting.
- Both choices save automatically, with individual resets and a reset for both text sizes.
- Navigation and toolbars reflow around larger text. Pet cards keep equal sizes and their progress bars stay below the labels.
- The minimap adapts its window size to fit larger text, respecting monitor bounds and keeping the current position when it fits. Locking, zoom and follow behavior remain available.

## Validation

Frontend preference/control tests, worker persistence tests and native minimap sizing tests cover independent settings, defaults, invalid values, DPI and monitor bounds. Enlarged settings, navigation, pet cards and recent souls were checked in isolated UI previews without changing saved player progress.
