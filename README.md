# Runwei Zhou — personal academic website

Plain static HTML and CSS. No build step, no dependencies, no JavaScript framework.
Upload the contents of this folder to the root of your GitHub Pages repo (or any web server) and it works.

## Files

```
index.html          About, education, industry experience, honors, skills, contact
research.html       Six research projects, grouped by lab
publications.html   Journal (J1–J3) and conference (C1–C5) papers, newest first
style.css           All styling
assets/
  Runwei_Zhou_CV.pdf   your CV (currently the Apr 2026 resume — replace when you update it)
  photo.jpg            optional headshot, see below
```

## Deploy to GitHub Pages

1. Copy these files into your repo (root level, not inside a subfolder).
2. `git add . && git commit -m "Add personal site" && git push`
3. Repo → Settings → Pages → Source: `Deploy from a branch`, branch `main`, folder `/ (root)`.
4. Live at `https://<username>.github.io/<repo>/` within a minute or two.

If the repo is named `<username>.github.io`, it serves from the bare domain instead.

## Add your headshot

Drop a square photo at `assets/photo.jpg` (600×600 or larger, JPG). It appears in the hero.
If the file is missing the portrait is removed automatically, so the page never shows a
broken image — nothing else to change.

## Things worth editing

- **Google Scholar / ORCID / GitHub** — add links next to email in the `contact-row` list in
  `index.html` (two places: hero and contact section) using the same `<li>` pattern.
- **"Last updated"** — footer of each page.
- **New papers** — copy an existing `<li>` block in `publications.html` and bump the index.
- **Job-market line** — the last paragraph of the About section says you're looking at faculty
  and research positions. Reword or delete once that changes.
- **Colors** — every color lives in the `:root` block at the top of `style.css`.
  `--accent` (deep blue) is the one to change if you want a different identity.

## Notes

- Fonts load from Google Fonts (Spectral, IBM Plex Sans, IBM Plex Mono). If you'd rather not
  depend on an external host, download them into `assets/fonts/` and swap the `<link>` for
  local `@font-face` rules.
- Prints cleanly: nav, footer, buttons, and the background field lines are hidden in print CSS.
- Responsive down to phone width, keyboard focus is visible, and `prefers-reduced-motion` is
  respected.
