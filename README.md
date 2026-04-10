# octanepizza

Moved the Apps Script HTML UI into this GitHub repo as `Index.html`.

## Files
- `gs.txt`: Google Apps Script server-side code (`Code.gs`).
- `Index.html`: Google Apps Script client-side HTML file.

- `index.html`: GitHub Pages entry file that redirects to `Index.html`.

## GitHub Pages note
- `Index.html` loads live data only when served by Google Apps Script (`google.script.run`).
- On GitHub Pages, the app now runs in demo mode with sample data so the UI is visible even without Apps Script backend access.

## Connect GitHub Pages to live Apps Script data
1. Deploy `gs.txt` code as a Web App in Google Apps Script (`Deploy` → `New deployment` → `Web app`).
2. Set access to `Anyone` (or your required audience) and copy the Web App URL.
3. In `Index.html`, set `window.GAS_WEB_APP_URL` before the app script loads, or run in browser console:
   - `localStorage.setItem('GAS_WEB_APP_URL', 'YOUR_WEB_APP_URL')`
   - then refresh the page.
4. GitHub Pages will call Apps Script via HTTP and show real data instead of demo data.
