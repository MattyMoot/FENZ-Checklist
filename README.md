# FENZ Install Checklist – install on your Android phone

The app is plain files with no server code, so any static host works. It needs **HTTPS** to install and run offline.

## Option A – GitHub Pages (free, about 5 minutes)
1. Create a new GitHub repository (it can be private if you have a paid plan; otherwise use a public repo).
2. Upload every file in this folder (index.html, manifest.webmanifest, sw.js, icon-192.png, icon-512.png).
3. Go to Settings → Pages → Source: "Deploy from a branch", choose `main` / root, then Save.
4. Open the URL it gives you (https://<you>.github.io/<repo>/) in **Chrome on your phone**.

## Option B – your own web server
Copy the folder into any HTTPS-served directory (nginx, Caddy, Cloudflare Pages, etc.).

## Install it on the phone
Open the URL in Chrome, tap ⋮ → **Add to Home screen / Install app**. It then opens full screen like a normal app and works with no signal.

## Where the data lives
Jobs and photos are stored **on the phone only** (in the browser's storage for that site). Export each job (Share or Download ZIP) to send it on.
Uninstalling the app or clearing Chrome's site data deletes the jobs.

## Changing the checklist
Open `index.html` and edit the `CHECKLIST` block near the top of the script. Each step is one line.
After you upload a change, bump `VERSION` in `sw.js` so phones pick up the new version.
