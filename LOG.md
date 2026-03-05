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

## 2026-03-06
- Reviewed `AGENTS.md`, `LOG.md`, and the current `index.html` implementation to assess product state and technical baseline.
- Identified key gaps across accuracy safeguards, transform preview fidelity, UI consistency, and maintainability.
- Produced a phased development plan covering stabilization, UX hardening, architectural refactor, and release readiness.

## 2026-03-06 (requirements update)
- Added explicit roadmap requirements for image zoom/pan in the image reference pane to improve precise GCP picking.
- Added explicit roadmap requirements for Satellite mode (imagery basemap toggle) to improve map-side reference matching speed and quality.
- Noted efficiency goal: reduce time-to-fit by improving point placement workflow and visual context during georeferencing.

## 2026-03-06 (feature implementation)
- Implemented image zoom controls (+, −, reset), mouse-wheel zoom, and pan support (Shift+drag, middle-drag, or right-drag) in the image reference pane.
- Updated image click handling to convert from viewport coordinates back to source pixel coordinates so GCP picks remain accurate while zoomed/panned.
- Added zoom status badge for quick scale awareness during referencing.
- Added Satellite (Esri) and Streets (OSM) basemap modes with a sidebar selector and Leaflet layer control; set Satellite as default.
- Performed diagnostics check on `index.html`; no file-level errors found.

## 2026-03-06 (overlay rotation bugfix)
- Fixed map preview bug where fitted images did not visually rotate/skew with affine parameters.
- Replaced axis-aligned `L.imageOverlay` bounds preview with a custom affine overlay layer that maps image pixels to map layer coordinates using transformed UL/UR/LL corners.
- Kept `fitBounds` behavior using all four transformed image corners for reliable framing after fit.
- Performed diagnostics check on `index.html`; no file-level errors found.
