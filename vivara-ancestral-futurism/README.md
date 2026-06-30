# VIVĀRA — Ancestral Futurism (Press)

A single-page, self-contained press release for the VIVĀRA *Ancestral Futurism*
ceremony at KRONOS, Japan. Static site — no build step, no framework.

Features the cymatics / Chladni "sand reveal" on each photograph, scroll-triggered
word highlighting, scroll-progress bar, and a click-to-play film embed.

## Structure

```
.
├── index.html              # the entire page (HTML + CSS + JS inline)
├── assets/
│   └── img/                # all photography + logo (referenced by index.html)
├── vercel.json             # static config + long-cache headers for /assets
└── README.md
```

Fonts (Cormorant Garamond, EB Garamond, Space Mono, Shippori Mincho) load at
runtime from Google Fonts. Everything else is local.

## Deploy to Vercel

**From GitHub (recommended)**
1. Create a new GitHub repo and push these files.
2. In Vercel: **Add New → Project → Import** the repo.
3. Framework Preset: **Other** (no build command, no output dir — it's static).
4. **Deploy.**

**Or from the CLI**
```bash
npm i -g vercel
vercel          # preview
vercel --prod   # production
```

**Or drag-and-drop:** zip this folder and drop it into the Vercel dashboard.

## Local preview

Serve over HTTP so the canvas sand effect can read the images:

```bash
npx serve .       # then open the printed http://localhost:3000
```

> Opening `index.html` directly with `file://` still shows every image, but some
> browsers disable the canvas pixel-read there, so the sand reveal falls back to
> a clean fade-in. Over HTTP (Vercel or `npx serve`) the full effect runs.

## Notes
- Press contact email in the release is a placeholder — update before publishing.
- To swap a photo, replace the file in `assets/img/` (keep the same filename) or
  update the path in `index.html`.
