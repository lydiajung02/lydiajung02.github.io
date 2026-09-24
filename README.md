# Data Analysis Portfolio

A simple static portfolio site (plain HTML/CSS/JS, no build step) modeled on the
[huhsu1.github.io](https://huhsu1.github.io/) layout: a landing page listing projects,
a Resume button, and per-project pages with a live demo plus the reasoning behind it —
tailored here to data analysis work (Chart.js demos, an interactive A/B test calculator, etc.).

## Structure

```
index.html                       landing page (project list)
resume.html                      placeholder resume page
projects/
  customer-churn-prediction.html
  covid19-trends-dashboard.html
  ab-test-checkout-funnel.html
  sales-forecasting.html
  nyc-housing-price-analysis.html
assets/
  css/style.css                  shared styles + light/dark theme
  js/theme.js                    dark mode toggle
  resume.pdf                     <- put your real resume here
```

All five projects currently ship with **placeholder content and synthetic demo data** —
swap in your real projects, numbers, and writeups before publishing.

## Preview locally

No build step needed. Either open `index.html` directly in a browser, or serve it:

```bash
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Customize

- **Name/email/links**: search-and-replace `example@example.com` and the footer/header
  blocks across `index.html`, `resume.html`, and each file in `projects/`.
- **Resume**: replace `assets/resume.pdf` with your actual PDF (create the `assets`
  folder file if it doesn't exist yet) — the download button on `resume.html` already
  points at that path.
- **Projects**: edit or delete the entries in `projects/`, and update the list in
  `index.html` to match. Each project page follows the same pattern: header/metrics →
  "Live Demo" → "How Did I Do This?" steps.
- **Colors/theme**: CSS variables are defined at the top of `assets/css/style.css`
  under `:root` (light) and `:root[data-theme="dark"]` (dark).

## Publish to GitHub Pages

Since the target is `lydiajung02.github.io`, GitHub serves this repo's `main` branch
root automatically once it's named exactly that:

```bash
git init
git add .
git commit -m "Initial data analysis portfolio"
git branch -M main
git remote add origin https://github.com/lydiajung02/lydiajung02.github.io.git
git push -u origin main
```

Then create the repo on GitHub first (name it exactly `lydiajung02.github.io`) if it
doesn't exist yet, before pushing. The site will be live at
`https://lydiajung02.github.io` within a minute or two of the push — no GitHub Pages
settings changes needed for a `username.github.io` repo (it's served automatically).

If you'd rather host it as a project page instead (e.g. `lydiajung02.github.io/portfolio`),
name the repo anything else and enable Pages for it in the repo's Settings → Pages,
serving from the `main` branch `/ (root)`.
