# NexusPOS

Offline-ready Point of Sale, packaged as an installable web app (PWA).

## Deploy on GitHub Pages
1. Create a new GitHub repository (e.g. `nexuspos`).
2. Upload **everything in this folder** (keep the `icons/` folder), or:
   ```
   git init
   git add .
   git commit -m "NexusPOS"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/nexuspos.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` / `(root)` → Save**.
4. After ~1 minute your app is live at `https://YOUR-USERNAME.github.io/nexuspos/`.

## Install from Chrome
- **Android:** open the link in Chrome → tap **📲 Install App** (bottom-left) or Chrome menu **⋮ → Install app**.
- **Desktop:** open the link → click the install icon in the address bar → **Install**.
- **iPhone/iPad:** open in Safari → Share → **Add to Home Screen**.

## Updating
Replace `index.html` on GitHub, then change `CACHE_VERSION` in `sw.js` (e.g. `v1` → `v2`) so installed copies refresh.

## Notes
- Data is stored in each device's browser (localStorage). Use the app's backup feature regularly.
- Works fully offline after the first visit. The QR and PDF libraries are cached automatically.
- Must be served over HTTPS (GitHub Pages does this) for install to work; opening `index.html` directly from a file won't offer install.
