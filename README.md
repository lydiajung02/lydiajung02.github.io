# Data Analysis Portfolio

A simple static portfolio site (plain HTML/CSS/JS, no build step) modeled on the
[huhsu1.github.io](https://huhsu1.github.io/) layout: a landing page listing projects,
a Resume button, and per-project pages with a live demo plus the reasoning behind it —
tailored to data analysis work (Chart.js demos, statistical write-ups, etc.).

## Structure

```
index.html                       landing page (project list)
resume.html                      resume page (real content, matches assets/resume.pdf)
projects/
  renewable-energy-emissions.html
  chatgpt-sentiment-nlp.html
assets/
  css/style.css                  shared styles + light/dark theme
  js/theme.js                    dark mode toggle
  resume.pdf                     generated resume PDF (regenerate via scripts below if you edit it)
```

## Preview locally

No build step needed. Either open `index.html` directly in a browser, or serve it:

```bash
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Known placeholders / things to finish

- The charts on both project pages are **illustrative/synthetic** reconstructions of the
  described results (matching shape, not your real numbers) — swap in real charts/output
  once you pull the actual notebooks over from wherever the original analysis lives.
- Each project page links to `https://github.com/lydiajung02` as a stand-in for the actual
  project repo/notebook — update those links once the real code has a home (ideally in
  this same repo, e.g. under a `notebooks/` folder).
- `resume.html` and `assets/resume.pdf` mirror your uploaded resume as of Sep 2026 — if you
  update the resume, edit `resume.html` and regenerate the PDF (a `reportlab`-based script
  was used; simplest path is re-exporting your resume doc as PDF directly and replacing
  `assets/resume.pdf`).

## Customize further

- **Projects**: edit or add entries in `projects/`, and update the list in `index.html` to match.
- **Colors/theme**: CSS variables are defined at the top of `assets/css/style.css`
  under `:root` (light) and `:root[data-theme="dark"]` (dark).

## Publish to GitHub Pages

This is set up for **https://github.com/lydiajung02/lydiajung-ds-portfolio** as a project
repo (not the special `username.github.io` repo), so it needs Pages enabled explicitly:

```bash
git remote add origin https://github.com/lydiajung02/lydiajung-ds-portfolio.git
git push -u origin main
```

Then on GitHub: **Settings → Pages** → Source: `Deploy from a branch` → Branch: `main`, folder `/ (root)`.
The site will be live at **https://lydiajung02.github.io/lydiajung-ds-portfolio/** a minute or two
after Pages is enabled.

(Create the repo on GitHub first, named exactly `lydiajung-ds-portfolio`, if it doesn't exist yet.)
