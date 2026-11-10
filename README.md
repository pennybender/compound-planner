# Compound Planner (offline version)

Your goal timeline and investment calculator as an app that runs on your iPhone with no internet.

## What's in this folder

- `index.html` — the app
- `sw.js` — keeps a copy of the app on your phone so it opens offline
- `manifest.webmanifest`, `*.png` — app name and Home Screen icon

## Set it up (once)

iPhone only lets a website work offline if it's served over https, so the folder has to go online once. GitHub Pages is free and permanent.

1. Make a free account at github.com.
2. Create a new repository, e.g. `compound-planner`. Set it to **Public** (free GitHub Pages needs that). The app files contain no personal data: your plan only ever lives on your phone and in backup files you keep.
3. Click **Add file → Upload files** and drag in every file from this folder. Click **Commit changes**.
4. Go to **Settings → Pages**. Under **Branch**, choose `main` and `/ (root)`, then **Save**.
5. After a minute or two the page shows your address, like `https://yourname.github.io/compound-planner/`.

## Put it on your iPhone

1. Open that address in **Safari**.
2. Tap **Share → Add to Home Screen → Add**.
3. Open it from the new icon once while online. From then on it works offline.

## Load your plan

Tap **Open file** (bottom of the Plan tab) and pick your `compound-planner-data.json`.

## Saving

- Changes save on your phone automatically as you go.
- **Save** also writes everything to your data file. On iPhone it opens the share sheet: tap **Save to Files**, pick the folder your data file is in, and tap **Replace**. On a computer in Chrome or Edge, Save updates the file directly after the first time.
- An orange dot on Save means there are changes not yet in your file.

## Where your data lives

- On your phone, inside the Home Screen app, and in your data file. It never goes to GitHub.
- Deleting the Home Screen app deletes the copy on your phone, so keep your data file in iCloud Drive.
- Never upload your data file to GitHub.

## Updating the app later

Upload the new `index.html` to the same repository, and change `VERSION` in `sw.js` (e.g. `cp-v2`). Your data isn't affected. The app picks up the new version next time it opens online.
