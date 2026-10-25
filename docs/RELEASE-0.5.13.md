# Waymark 0.5.13

## Clearer pet spawn locations

- Each creature has a consistent spawn color. The outer ring of its area portrait matches its nearby reference points and soft spawn patches.
- At medium zoom, colored points and subtle patches keep the terrain readable. Zoom closer to see creature portraits on individual spawn references.
- Crowded same-creature references group with a count. Overlapping portraits separate with short leader lines back to their reference coordinates.
- The main portrait retains its rank color and rank badge. Creature identity colors stay consistent when the pet levels up.
- Both the main map and minimap use the new display, with more compact grouping on the minimap.

These remain reference locations, not a live mob-availability feed. Soft patches illustrate nearby references; they do not claim an exact movement range or connect distant locations across empty terrain. Existing pet filters and completion settings still control what appears.

## Validation

180 frontend tests cover source-count preservation, species separation, stable identity colors, zoom detail, overlapping portraits and existing map behavior. Main-map and compact minimap rendering were checked in isolated previews using bundled reference data.
