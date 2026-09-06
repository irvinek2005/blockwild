# Blockwild Survival v2

This is a portable Safari/PWA prototype built from the uploaded Blockwild
prototype.

## What changed

- Added a Minecraft-style title screen.
- Added random and custom world seeds.
- Added Survival and Creative world selection.
- Added deterministic terrain generation from the seed.
- Added 16×16 chunk loading with a five-by-five active chunk window.
- Added basic chunk unloading as the player explores.
- Added local save/continue for the current seed and player state.
- Added basic horizontal collision.

## Run it

Serve this folder from an HTTPS static host, then open the URL in Safari.
The Three.js module is still loaded from jsDelivr in this milestone, so a
first launch requires an internet connection.

This milestone intentionally does not claim full world-edit persistence,
combat, or multiplayer yet. Those are the next systems to build on top of the
seed and chunk foundation.