# 📱 Put "Our Learning Web" on the iPad — 10 minutes

The iPad can't run an HTML file as an app directly (Apple only installs apps from
the App Store or from a **web address** via Safari). So we put the app's folder
on a free static host once, then "install" it from Safari. After the first visit
it works **fully offline** — the service worker keeps a copy on the iPad.

## What's in this package

| File | Purpose |
|---|---|
| `index.html` | The entire app |
| `manifest.webmanifest` | App name, colors, icons for installing |
| `sw.js` | Service worker — makes it work offline |
| `icon-192.png`, `icon-512.png` | App icons (Android/desktop) |
| `apple-touch-icon.png` | The icon iPadOS uses on the Home Screen |

Keep all files together in one folder. Don't rename `index.html`.

## Step 1 — Host it free on GitHub Pages (one-time)

1. Create a free account at **github.com** (skip if you have one).
2. Top-right **+** → **New repository** → name it `learning-web` → set **Public** → **Create repository**.
3. Click **uploading an existing file**, drag in ALL the files from this package, press **Commit changes**.
4. Go to **Settings → Pages** (left sidebar). Under *Build and deployment*, set
   **Source: Deploy from a branch**, **Branch: main**, folder `/ (root)` → **Save**.
5. Wait ~1 minute, refresh the page — you'll see your link:
   `https://YOURNAME.github.io/learning-web/`

*Alternative hosts that work the same way: Netlify (drag-and-drop deploy), Cloudflare Pages, Vercel.*

## Step 2 — Install on the iPad

1. Open **Safari** on the iPad and go to your link.
2. Tap the **Share** button (square with the up arrow).
3. Tap **Add to Home Screen** → **Add**.

That's it. You now have a **Learning Web** icon that launches full-screen —
no browser bars, sound and touch fully working, and it runs **without internet**
after that first load. Star progress is saved on the iPad itself.

## Updating the app later

When I give you a new version, just replace `index.html` in the GitHub repo
(upload again with the same name → Commit). On the iPad, open the app while
online once; it picks up the new version on the next launch.
If it seems stuck on the old one: Settings → Safari → Advanced → Website Data →
delete your site's entry, then reopen.

## Good to know

- **Progress lives on the device.** Each iPad/browser keeps its own stars.
- **The teacher voice** uses the iPad's built-in Siri voices — it works offline
  and sounds quite good on iPadOS.
- Don't delete the Home Screen icon casually: iPadOS clears that app's saved
  stars when you remove it.
- The same link works on any phone, tablet, or computer — it's your app now.
