# Blockwild — GitHub Pages Build

## Publish on GitHub Pages

1. Create a new GitHub repository named `blockwild`.
2. Upload **all files and folders from this project**, including the hidden `.github` folder.
3. Commit them to the `main` branch.
4. Open the repository's **Settings → Pages**.
5. Under **Build and deployment → Source**, choose **GitHub Actions**.
6. Open the **Actions** tab and wait for `Deploy Blockwild to GitHub Pages` to finish.
7. Your game will then be available at:

   `https://YOUR-GITHUB-USERNAME.github.io/blockwild/`

## iPhone

Open the GitHub Pages URL in Safari, rotate to landscape, then choose:

**Share → Add to Home Screen**

Your persistent save data is stored by Safari for that specific GitHub Pages URL.

---

# Blockwild Safari v3 — Persistent Worlds

This build is designed for Safari on iPhone when hosted over HTTPS (Replit is suitable).

## v3 changes
- Mined blocks stay mined after chunks unload/reload.
- Placed blocks stay placed after chunks unload/reload.
- World edits persist after closing and reopening Safari.
- Inventory persists.
- Hotbar selection/layout persists.
- Player position, health, hunger, mode and world time persist.
- Autosaves after edits, every 30 seconds, when Safari is backgrounded, and when the page closes.
- Service worker caches runtime resources after a successful online load.
- Three.js has a jsDelivr primary source plus an UNPKG fallback.

## Replit
Upload the contents of this folder to your Replit project and serve it as a static website.
Open the HTTPS Replit URL in Safari.

For the app-like experience:
Safari > Share > Add to Home Screen.

## Offline note
Open the hosted game successfully while online first. The service worker will cache the app
and the Three.js module it used. Safari storage/cache may still be evicted by iOS if storage
pressure is high, so keep the Replit deployment available.

## Save data
Save data is stored by Safari for the site origin. Clearing Safari website data, changing to a
different Replit domain, or deleting the Home Screen web app can remove local save data.

Blockwild is an original voxel sandbox prototype and does not contain Minecraft proprietary assets.
