# GM Media — website

Static three-page site. No build step, no dependencies to install.

```
index.html            Home
gages-story.html      Gage's Story
financial-model.html  Financial Model
support.js            page runtime
image-slot.js         image placeholder component
assets/               video, poster frames, logos, client photos
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

## Deploy on Vercel

In Vercel: **New Project → import the repo → Framework Preset "Other" → Deploy.**
Leave the build command and output directory empty; the files are served as-is.
Every push to `main` redeploys.

Or without GitHub, from this folder: `npx vercel --prod`

## Notes

- Needs internet at page load: React and the Google Fonts (Archivo, IBM Plex Mono) load from CDNs.
- The Calendly booking widget on Home is an iframe embed; no keys required.
- Total size is about 10 MB, nearly all of it b-roll video under `assets/broll/`.
- Videos are already trimmed and compressed for web. If you swap one in, keep it under ~1 MB and add a matching poster frame in the same folder.
