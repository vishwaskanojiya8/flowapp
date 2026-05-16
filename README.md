# TaskFlow PWA — Deployment Guide

## What's in this folder
```
taskflow-pwa/
├── index.html       ← The full app
├── manifest.json    ← PWA manifest (name, icons, colors)
├── sw.js            ← Service worker (offline support)
└── icons/           ← App icons for all devices
    ├── icon-72.png
    ├── icon-96.png
    ├── icon-128.png
    ├── icon-144.png
    ├── icon-152.png
    ├── icon-192.png
    ├── icon-384.png
    └── icon-512.png
```

---

## Option A — Netlify (Easiest, 2 minutes)

1. Go to https://app.netlify.com
2. Sign up free (use GitHub/Google)
3. Drag & drop the entire `taskflow-pwa` **folder** onto the Netlify dashboard
4. You get a live HTTPS URL instantly (e.g. `https://taskflow-abc123.netlify.app`)
5. Open that URL on your phone → install prompt appears!

---

## Option B — GitHub Pages

1. Create a free account at https://github.com
2. Create a new repository called `taskflow-pwa` (set to Public)
3. Upload all files from this folder to the repo
4. Go to Settings → Pages → Source: main branch → Save
5. Your app is live at `https://yourusername.github.io/taskflow-pwa`

---

## Option C — Vercel

1. Go to https://vercel.com → Sign up free
2. Install Vercel CLI: `npm i -g vercel`
3. In this folder, run: `vercel`
4. Follow prompts → live in seconds

---

## Installing the App on Your Device

### Android (Chrome)
1. Open your hosted URL in Chrome
2. Tap ⋮ menu → "Add to Home Screen"
3. Tap "Install"
4. App appears on your home screen like a native app!

### iPhone / iPad (Safari)
1. Open your hosted URL in **Safari** (must be Safari, not Chrome)
2. Tap the Share button (box with arrow)
3. Scroll down → "Add to Home Screen"
4. Tap "Add"

### Windows / Mac / Linux (Chrome or Edge)
1. Open your hosted URL
2. Click the install icon (⊕) in the address bar
3. Click "Install"
4. App opens in its own window, appears in taskbar/dock

---

## Features
- ✅ Works fully offline after first load
- ✅ Your data is saved (tasks, notes, users persist)
- ✅ Looks and feels like a native app (no browser UI)
- ✅ Fast loading via service worker cache
- ✅ Install prompt appears automatically on Android/Desktop
- ✅ App shortcuts: long-press icon to jump to "Add Task" or "Notes"

---

## Updating the App
Just re-upload `index.html` to your host. The service worker will
automatically fetch the new version in the background and apply it
on next app open.
