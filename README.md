# octanepizza

Migrated the Apps Script HTML UI into this GitHub repo as a GitHub Pages app.

## Files
- `gs.txt`: Google Apps Script server-side code (`Code.gs`).
- `index.html`: Primary GitHub Pages entry file (full app UI).
- `Index.html`: Compatibility redirect to `index.html`.

## GitHub Pages note
- `index.html` loads live data when served inside Google Apps Script (`google.script.run`).
- On GitHub Pages, the app runs in demo mode with sample data so the UI is still usable without Apps Script backend access.

## Connect GitHub Pages to live Apps Script data
1. Deploy `gs.txt` code as a Web App in Google Apps Script (`Deploy` → `New deployment` → `Web app`).
2. Set access to `Anyone` (or your required audience) and copy the Web App URL.
3. In `index.html`, set `window.GAS_WEB_APP_URL` before the app script loads, or run in browser console:
   - `localStorage.setItem('GAS_WEB_APP_URL', 'YOUR_WEB_APP_URL')`
   - then refresh the page.
4. GitHub Pages will call Apps Script via HTTP and show real data instead of demo data.
