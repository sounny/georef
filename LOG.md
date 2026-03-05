# Agent Log

## 2025-08-12
- Created `AGENTS.md` with project description and logging instructions.
- Added `LOG.md` to track future work.
- Implemented initial in-browser georeferencing prototype in `index.html`.
- Added visual feedback for control points with image dots and map markers.

## 2026-03-05
- Performed a comprehensive UI redesign of the georef app using modern dark-theme aesthetics (Inter font, glassmorphism, dynamic animations).
- Implemented Basemap switching functionality via Leaflet layer control, explicitly adding Esri World Imagery (Aerial) as the default per user request.
- Improved the layout to be flexible (not restricted to a 420px sidebar).
- Enhanced UX with numbered ground control points (GCPs) on both map and table, clear error states, and guided step-by-step instructions.
- Added support for adjusting the opacity of the transformed overlay.
- Handled JP2 explicitly by notifying the user they need to convert to an allowed format (like JPG).
