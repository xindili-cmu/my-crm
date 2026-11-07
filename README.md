# Atlas CRM

Single-file CRM front end (`index.html`) backed by a Google Sheet through a Google Apps Script web app.

## Setup

The Google Sheet connection is left blank in this repo. To connect your own:

1. Deploy your Apps Script as a web app and copy its URL (ends in `/exec`).
2. In `index.html`, find the `Config: Apps Script` section and fill in:
   ```js
   const APPS_SCRIPT_URL = 'https://script.google.com/macros/s/.../exec';
   const TOKEN = 'your-token';
   ```
3. Open `index.html` in a browser.

Until these are set, the page loads but shows a "backend not configured" error instead of data.
