# NovaWise Syndicate — Static Site

Official homepage for NovaWise Syndicate (nWs).
React + Vite, Tailwind CSS v4, Framer Motion, 4-language i18n (EN / ZH / FR / ES).

## Deploy to GitHub Pages

### Option A — GitHub Web UI (easiest)

1. Create a new GitHub repository
2. Upload the contents of this zip (not the zip itself) to the repository root
3. Go to **Settings → Pages → Deploy from branch → main → / (root)**
4. Save — your site will be live at `https://YOUR_USERNAME.github.io/YOUR_REPO/`

### Option B — Push from CLI

Unzip the files, then from that folder:

```
git init
git add .
git commit -m "deploy NovaWise Syndicate homepage"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

Then enable Pages in Settings → Pages as above.

### Option C — Existing repo, gh-pages branch

If you have a repo already and want to deploy from a `gh-pages` branch, push
only the static files there and point Pages to that branch.

## Routing

All navigation uses **hash routing** so every link works with no server config:

| URL fragment | Page |
|---|---|
| `#/` | Home |
| `#/blog` | Blog |
| `#/projects` | Projects |
| `#/projects/minecraft` | Minecraft |
| `#/projects/creative-tools` | Creative Tools |
| `#/iwde` | IWDE Event |

## Dynamic IWDE Countdown

Automatically adjusts every year — no code changes needed:

- **Before July 1** — live countdown (days / hours / min / sec) to opening day
- **July 1 – 4** — green "Live Now" banner with pulsing indicator
- **After July 4** — countdown resets to the next year's July 1

The edition name (IWDE26, IWDE27 …) also updates automatically.
Everything runs in the browser; no server or API required.
