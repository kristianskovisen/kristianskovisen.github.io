# Kristian Skov Isen — academic website

A single-page academic site (plain HTML + CSS, no build step) for GitHub Pages.

## Files

```
index.html      The page
style.css       All styling (the "task space" design system)
assets/         Put your PDFs here (see below)
.nojekyll       Tells GitHub Pages to serve files as-is
README.md       This file
```

## 1. Add your PDFs

Drop these two files into the `assets/` folder using **exactly** these names
(the buttons on the page already point at them):

| File to add                                    | What it is        |
| ---------------------------------------------- | ----------------- |
| `assets/isen_product_relatedness_in_tasks.pdf` | The paper draft   |
| `assets/isen_product_relatedness_slides.pdf`   | The CEFAU slides  |
| `assets/portrait.jpg`                          | Your photo        |

For the photo, use a roughly square image named exactly `portrait.jpg`. Until you
add it, the header shows a small "Photo" placeholder box.

## 2. Edit the placeholders

Open `index.html` and update:

- **Email** — the header links to `mailto:kristian.isen@econ.au.dk`. Change it to
  your real address if that isn't it.
- **LinkedIn** — currently `linkedin.com/in/kristianskovisen/`; correct it if your
  profile URL differs.

Everything else (name, title, department, abstract) is already filled in from
your paper.

## 3. Publish on GitHub Pages

**Option A — personal site (nicest URL: `https://<username>.github.io`)**

1. Create a repo named exactly `<username>.github.io`.
2. Commit these files to the `main` branch (index.html at the repo root).
3. GitHub Pages turns on automatically. Visit `https://<username>.github.io`.

**Option B — project repo (URL: `https://<username>.github.io/<repo>`)**

1. Create any repo (e.g. `website`) and commit these files.
2. Repo **Settings → Pages → Build and deployment**.
3. Source: **Deploy from a branch**, Branch: **main**, Folder: **/ (root)**, Save.
4. Wait ~1 minute, then open the URL it shows.

### Commit from the command line

```bash
git init
git add .
git commit -m "Academic website"
git branch -M main
git remote add origin https://github.com/<username>/<repo>.git
git push -u origin main
```

## Preview locally

```bash
# from inside this folder
python3 -m http.server 8000
# then open http://localhost:8000
```

## Notes

- Fonts (Fraunces, Newsreader, IBM Plex Mono) load from Google Fonts, so the site
  needs to be viewed online to show them; offline it falls back to system serifs.
- The page is responsive, keyboard-accessible, and respects reduced-motion.
- To change accent colors, edit the variables at the top of `style.css`
  (`--anchor` and `--accent`).
