# North America Uncovered

A single-player geography game with 25 destinations, ArcGIS 3D terrain, photos, clues, and multiple-choice questions.

## Publish

Upload the contents of this folder to the folder served by your GitHub Pages site. Keep `index.html` at that folder’s root and preserve the `images` folder. All local references use relative paths, so the app can run under a repository subpath. No build step, backend, ChatGPT connection, or API key is needed.

## Files

- `index.html`: page structure and script loading
- `styles.css`: appearance and layout
- `app.js`: game logic and ArcGIS scene
- `landmarks.js`: destinations, coordinates, clues, explanations, and factual source links
- `photos.js`: image paths and photo credits/licenses
- `images/`: 25 reference photos
- `.nojekyll`: serves these files without Jekyll processing

Internet access is required for the ArcGIS SDK, imagery, and terrain services. Map imagery is static imagery, not live conditions. Photo attribution and source/license links remain available in the game; retain them when publishing.

## Preview locally

Run `python3 -m http.server 8000` from this folder, then open http://localhost:8000 in a browser.

## Editing

Keep destination order in `landmarks.js` aligned with the numeric photo keys in `photos.js`. JavaScript calculates quiz totals from the destinations; visible introductory counts in `index.html` also need updating when changing the number of stops.
