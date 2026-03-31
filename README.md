# VIVARA Tokyo — Working Document

A self-contained single-page app for the VIVARA Tokyo Launch Dinner.
Tabs: Menu · Shot List · Space · Chef Notes · Supply List · Senses

## Deploy to Vercel (3 ways)

---

### Option A — Vercel CLI (fastest, ~60 seconds)

```bash
# 1. Install Vercel CLI if you don't have it
npm install -g vercel

# 2. From inside this folder:
cd vivara-tokyo-vercel
vercel

# 3. Follow the prompts:
#    - Link to existing project? No
#    - Project name: vivara-tokyo (or anything)
#    - Directory: ./  (current)
#    - Override settings? No

# 4. Vercel gives you a live URL immediately.
# To deploy to production URL:
vercel --prod
```

---

### Option B — Drag & Drop (no CLI needed)

1. Go to **vercel.com** → Log in
2. Click **Add New → Project**
3. Choose **"Import from folder"** or drag the entire `vivara-tokyo-vercel` folder onto the page
4. Leave all settings as default → **Deploy**
5. Done — live URL in ~10 seconds

---

### Option C — GitHub (auto-deploys on every update)

1. Create a new GitHub repo (can be private)
2. Push this folder to the repo:
   ```bash
   git init
   git add .
   git commit -m "VIVARA Tokyo working doc"
   git remote add origin https://github.com/YOUR_USERNAME/vivara-tokyo.git
   git push -u origin main
   ```
3. Go to vercel.com → **Add New → Project → Import Git Repository**
4. Select the repo → Deploy
5. Every `git push` auto-redeploys

---

## Custom Domain (optional)

In Vercel dashboard → Project → Settings → Domains → Add `tokyo.vivaradrops.com`

---

## File Structure

```
vivara-tokyo-vercel/
├── index.html     ← entire app (self-contained, no build step)
├── vercel.json    ← Vercel config
└── README.md      ← this file
```

Everything is embedded — no external assets, no build process, no Node.js required.
The only external call is Google Fonts (loaded from fonts.googleapis.com).

---

*VIVARA — Tokyo Launch Dinner — Confidential Working Document*
