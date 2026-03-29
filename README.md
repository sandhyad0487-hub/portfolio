# Sandhya | Portfolio Website

A personal portfolio website hosted on Render with manual CI/CD via GitHub Actions.

## 🗂️ Project Structure

```
sandhya-portfolio/
├── index.html                        ← Main portfolio page
├── my.jpeg                           ← Profile photo (large)
├── my2.jpeg                          ← Profile photo (small)
├── my1.jpeg                          ← Additional photo
├── fro.jpeg                          ← Certificate image
├── aws (1).jpeg                      ← AWS certificate
├── git.jpeg                          ← Git certificate
├── tq.jpeg                           ← Project screenshot
├── quz.jpeg                          ← Project screenshot
├── gam.jpeg                          ← Project screenshot
├── .gitignore                        ← Git ignore rules
├── README.md                         ← This file
└── .github/
    └── workflows/
        └── deploy.yml                ← GitHub Actions manual deploy
```

## 🚀 Hosting on Render

### First-time Setup

1. Push this repo to GitHub
2. Go to [render.com](https://render.com) → **New** → **Static Site**
3. Connect GitHub and select this repo
4. Settings:
   - **Branch:** `main`
   - **Build Command:** *(leave blank)*
   - **Publish Directory:** `.`
5. Click **Create Static Site**

### Setting Up Manual Deploy (GitHub Actions)

1. In Render dashboard → your site → **Settings** → **Deploy Hooks**
2. Create a hook named `github-actions` and copy the URL
3. In GitHub repo → **Settings** → **Secrets and variables** → **Actions**
4. Add secret: `RENDER_DEPLOY_HOOK_URL` = *paste the Render hook URL*

### How to Deploy

1. Go to GitHub repo → **Actions** tab
2. Click **"Deploy to Render (Manual)"**
3. Click **"Run workflow"** → add optional reason → **Run workflow**
4. Watch it complete, then check Render dashboard for the live deploy

## 🛠️ Tech Stack

- Pure HTML, CSS, JavaScript (no framework/build step needed)
- Supabase for contact form backend
- Render Static Site for hosting
- GitHub Actions for manual CI/CD

## ⚠️ Notes

- Images must be in the root folder alongside `index.html`
- Supabase anon key is intentionally public — ensure RLS is enabled on your `backend` table
- Deploy is **manual only** — it will NOT auto-deploy on every push
