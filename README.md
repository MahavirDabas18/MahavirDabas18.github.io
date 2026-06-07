# Mahavir Dabas — Personal Academic Website

A minimal, single-page academic website (plain HTML + CSS, no build step).

## Quick preview (local)

Just open `index.html` in your browser, or run a tiny server:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages

1. Create a repo. For a personal site at `https://<username>.github.io`,
   name it **`<username>.github.io`**. (Otherwise it lives at
   `https://<username>.github.io/<repo-name>/`.)
2. Push these files to the repo:
   ```bash
   git init
   git add .
   git commit -m "Initial website"
   git branch -M main
   git remote add origin https://github.com/<username>/<repo>.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from
   a branch**, pick `main` / `root`, save. Your site is live in ~1 minute.

## What to edit

| Thing | Where |
|-------|-------|
| Bio, news, publications text | `index.html` |
| Social/CV links (`href="#"`) | `index.html` — top of file, `social-links` and each pub |
| Colors, fonts, spacing | `style.css` — the `:root` variables at the top |
| Your photo | replace `images/profile.jpg` (square image works best) |
| Paper thumbnails | replace `images/pub1.png` … `pub5.png` (wide, ~280×180) |
| CV | drop `cv.pdf` into `assets/` (the CV icon already links to `assets/cv.pdf`) |
| Favicon | replace `images/favicon.png` |

All current images are **placeholders** — swap them for your own.

> Remember to fill in the real URLs for the `href="#"` links (Google Scholar,
> LinkedIn, GitHub, and each paper).

## Structure

```
mahavir_personal_web/
├── index.html       # all page content
├── style.css        # all styling
├── .nojekyll        # tells GitHub Pages to serve files as-is
├── images/          # profile photo, paper thumbnails, favicon
└── assets/          # put cv.pdf here
```
