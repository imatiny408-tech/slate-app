# Slate

A calm, minimal planner for iPad: a Home dashboard, three calendar layouts (big date, list with Routines, week planner), routines you drag into your day, an idea board and a daily feeling check-in.

**Live app:** https://imatiny408-tech.github.io/slate-app/

## Install on iPad
Open the live app in Safari, tap Share, then **Add to Home Screen**. Use Slate from that icon: it opens full screen, works offline, and the iPad keeps its data.

## Your data
Everything is saved on the device, in the browser's storage for this site. There's no account yet.
- Updates to the app never erase it. Each update only replaces the app's code.
- To move data between devices, or out of the Claude version, use **Settings → Back up or restore data**.

## How updates go live
Every push to `main` runs `.github/workflows/deploy.yml`, which builds `dist/` with `tools/build.py` and publishes it to GitHub Pages. The app picks up the new version the next time it's opened.

## Project layout
- `src/slate.html`: the whole app (the same page that's published as the Claude artifact)
- `public/`: icons and the web app manifest
- `tools/build.py`: wraps the page into an installable web app in `dist/`
- `tools/sw.template.js`: offline support; network first so updates always arrive
