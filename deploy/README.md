# GM Media — website

Static four-page site. No build step, no dependencies to install.

```
index.html               Home
gages-story.html         Gage's Story
client-breakdowns.html   Client Breakdowns
financial-model.html     Financial Model
practice-map.html        Practice map (embedded in Client Breakdowns)
support.js               page runtime
image-slot.js            image placeholder component
assets/                  video, poster frames, logos, client photos
```

## Import into GitHub

Create an empty repo, then from inside this folder:

```bash
git init
git add .
git commit -m "GM Media website"
git branch -M main
git remote add origin https://github.com/<you>/<repo>.git
git push -u origin main
```

## Deploy

GitHub Pages: repo **Settings → Pages → Deploy from a branch → main / root.**

Vercel: **New Project → import the repo → Framework Preset "Other" → Deploy.**
Leave the build command and output directory empty; the files are served as-is.
Every push to `main` redeploys.

## Notes

- Needs internet at page load: React and the Google Fonts (Archivo, IBM Plex Mono) load from CDNs.
- The Calendly booking widget is an iframe embed; no keys required.
- Case study videos are Vimeo embeds; the practice map is a local iframe.
- Total size is about 11 MB, nearly all of it b-roll video under `assets/broll/`.
- Videos are already trimmed and compressed for web. If you swap one in, keep it under ~1 MB and add a matching poster frame in the same folder.
