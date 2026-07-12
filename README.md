# BulkLog

Offline-first nutrition & weight tracking PWA. No backend, no build step — pure static files. All data lives in the browser's `localStorage` on the device.

## Deploy to GitHub Pages

1. Create a new GitHub repo (e.g. `bulklog`).
2. Upload all files in this folder to the repo root, keeping the `icons/` folder structure:
   ```
   index.html
   manifest.json
   sw.js
   icons/icon-180.png
   icons/icon-192.png
   icons/icon-512.png
   icons/favicon-32.png
   ```
3. Go to **Settings → Pages** in the repo.
4. Under **Source**, select the branch (usually `main`) and folder `/ (root)`, then **Save**.
5. GitHub will give you a URL like `https://yourusername.github.io/bulklog/`. Wait a minute or two for it to go live.

## Install on iPhone

1. Open the GitHub Pages URL in **Safari** (must be Safari, not Chrome, for install to work).
2. Tap the **Share** icon → **Add to Home Screen**.
3. Launch it from the home screen icon — it opens full-screen with no browser bar, and works offline after the first load.

## Notes

- Because it's served over HTTPS (GitHub Pages default), the service worker and installability will work correctly — this wasn't guaranteed when opening the file directly (`file://`).
- All data (meal plan, logs, weight, settings, reminders) stays in `localStorage` on that specific device/browser. Use **Settings → Backup as JSON** to move data between devices.
- To update the app later, just edit `index.html` and push — the service worker will fetch the new version on next load.
