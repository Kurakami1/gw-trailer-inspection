GW Trailer Inspection — PWA package

Files:
- index.html: original v5 inspection app, with PWA metadata and service-worker registration
- app.webmanifest: install name, standalone display and Android icons
- sw.js: offline app shell + runtime caching for external libraries/fonts after first successful load
- icons/: app icons

IMPORTANT:
1. Upload the CONTENTS of this folder to an HTTPS static host (not the ZIP itself as the app).
2. Open the HTTPS address in Chrome on Android, wait for the page to load fully once while online.
3. Chrome menu (⋮) -> Install app / Add to Home screen.
4. Open the installed app once while online so external libraries, fonts and styles can be cached.

The app stores inspection settings/history/PDF archive in the browser's local storage/IndexedDB on that device and browser profile. It does not sync the archive to a server. Keep using the same installed app/browser profile; clearing site data can erase local records. ZIP backup remains recommended.

Offline limitation:
The core app shell is cached. External CSS/JS/font assets are cached as they are first requested, so do the first full load while online. If a particular external asset was not cached before going offline, that feature or styling may be unavailable until connectivity returns.
