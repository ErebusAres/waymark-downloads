# Waymark 0.5.15

- Pet locations now use readable farming-pocket icons on both the main map and minimap. Colliding pockets share a numbered badge; click it to choose a creature from a scrollable list with icons, names and ranks. The badge number counts distinct creatures, not spawn points.
- Selecting or hovering a creature reveals its mapped spawn references as quiet dots and a subtle tint. Other creatures remain visible. The existing Always show spawns option retains all-reference display for users who want it.
- Icons keep a consistent screen size as you zoom, with more room at larger text sizes. Zooming in separates nearby pockets. Grouping changes only the display: source coordinates, pocket IDs and routes remain intact.
- Pets can be filtered by World farming or Boxes & rewards only. The latter includes pets with a chest/reward source and no recorded world drop or farming area in the bundled catalog; it does not prove that another source cannot exist. Selecting it clears the map filter so these pets are visible.
- Farming routes now offer Completion priority or Nearby first. Routes use explicitly selected pets and the planner map, independently of the Pets page filters. Saving a route frames every stop and shows numbered markers on the map. Stop order remains editable in Circuit.
- New filter and route-order preferences are saved and included in backups. Existing preferences, rank colors, recommendation stars, minimap lock and non-pet layers are preserved.

Route connections are straight-line guidance, not terrain-aware navigation. Mob locations are reference positions, not live spawn availability. No game-reader protocol changes are included in this update.
