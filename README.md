# octanepizza

Migrated the Apps Script HTML UI into this GitHub repo as a GitHub Pages app.

## Files
- `gs.txt`: Google Apps Script server-side code (`Code.gs`).
- `index.html`: Primary GitHub Pages entry file (full app UI).
- `Index.html`: Compatibility redirect to `index.html`.

## GitHub Pages note
- To write directly to Google Sheets from GitHub Pages, you must connect your Apps Script Web App URL.
- Use the in-app **Set Backend URL** button or add `?gas_web_app_url=YOUR_WEB_APP_URL` to the page URL.
- Once connected, create/update actions are sent to Apps Script (and then to Google Sheets).
- The current default URL is already set in `index.html` as `DEFAULT_GAS_WEB_APP_URL`.

## Connect GitHub Pages to live Apps Script data
1. Deploy `gs.txt` code as a Web App in Google Apps Script (`Deploy` → `New deployment` → `Web app`).
2. Set access to `Anyone` (or your required audience) and copy the Web App URL.
3. Configure the backend URL using either method:
   - Add a query param once: `?gas_web_app_url=YOUR_WEB_APP_URL` (this is saved to `localStorage` automatically).
   - Or in browser console run:
   - `localStorage.setItem('GAS_WEB_APP_URL', 'YOUR_WEB_APP_URL')`
   - then refresh the page.
4. GitHub Pages will call Apps Script via HTTP and show real data instead of demo data.
