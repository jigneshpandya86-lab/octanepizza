# octanepizza

Moved the Apps Script HTML UI into this GitHub repo as `Index.html`.

## Files
- `gs.txt`: Google Apps Script server-side code (`Code.gs`).
- `Index.html`: Google Apps Script client-side HTML file.

- `index.html`: GitHub Pages entry file that redirects to `Index.html`.

## GitHub Pages note
- `Index.html` loads live data only when served by Google Apps Script (`google.script.run`).
- On GitHub Pages, the app now runs in demo mode with sample data so the UI is visible even without Apps Script backend access.
