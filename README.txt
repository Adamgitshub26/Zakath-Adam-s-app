ZAKAT LEDGER — how to put it on your phone
==========================================

WHAT'S IN THIS FOLDER
  index.html            the whole app
  manifest.webmanifest  makes it installable
  sw.js                 lets it work offline
  icon-192.png          app icons
  icon-512.png
Keep all files together in one folder.

────────────────────────────────────────────
FASTEST WAY TO HOST IT (free, ~2 minutes)
────────────────────────────────────────────
1. Go to  https://app.netlify.com/drop
2. Drag this WHOLE folder onto the page.
3. Netlify gives you a link like  https://your-name.netlify.app
   That link is your app. Open it on your phone.

(Other free options that work the same way: Vercel, Cloudflare
Pages, or GitHub Pages. Any static host will do. It MUST be https
for offline + install to work — Netlify Drop already is.)

────────────────────────────────────────────
INSTALL IT TO YOUR HOME SCREEN
────────────────────────────────────────────
iPhone / iPad (Safari):
  Open the link → tap Share → "Add to Home Screen".

Android (Chrome):
  Open the link → an "Install" button appears in the app, or use
  the ⋮ menu → "Install app" / "Add to Home screen".

Once added it opens full-screen with its own icon, like a normal app,
and keeps working with no internet.

────────────────────────────────────────────
GOOD TO KNOW
────────────────────────────────────────────
• Your entries are saved in that browser's storage on your device.
  They stay between visits, but they do NOT sync to other devices,
  and clearing the browser's site data will erase them.
• BACKUP: open the year menu → Backup → "Export backup" to save all
  your data to a .json file (keep it in your files, email it to
  yourself, etc.). "Import file" restores from one of those files —
  it replaces whatever is currently on the device. Export now and
  then before switching phones or clearing your browser.
• To try it locally first (on a computer) without hosting:
      cd into this folder
      python3 -m http.server 8000
  then open  http://localhost:8000
  (Opening index.html by double-click also runs the app, but the
  offline service worker only registers over http/https.)
