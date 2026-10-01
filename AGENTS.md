# Base44 Setup Notes

## Project Overview
Single-file static HTML app ("Jonny's Academic Time Tracker") — no build step, no backend, no external dependencies beyond CDN-loaded Tailwind CSS, Google Fonts, and FontAwesome. All logic is inline JavaScript in `index.html`.

## Running the App
```
docker compose -f docker-compose.base44.yml up -d
```
Serves `index.html` via nginx:alpine on port 3000. No environment variables or secrets required.

## Editing
All changes go directly in `index.html`. Since nginx serves the file from a bind mount, edits are reflected immediately — call `reload_preview` after changes to refresh the browser.
