# 👋 Welcome to Lydia Jung's Portfolio

**Live site: [lydiajung02.github.io](https://lydiajung02.github.io/)**

A static portfolio site (plain HTML/CSS/JS, no build step) modeled on the
[huhsu1.github.io](https://huhsu1.github.io/) layout: a landing page listing projects, a Resume
button, and per-project pages with a live demo plus the reasoning behind it.

---

## About Me

- UC Berkeley, B.S. in Data Science, Domain Emphasis on Cognition
- Aspiring Data Analyst / Data Scientist
- Interested in data-driven decision making, data visualization, and statistical modeling

## Featured Projects

| Project | Type | Summary |
|--------|------|---------|
| [U.S. Renewable Energy & Emissions Analysis](projects/renewable-energy-emissions.html) | Notebook, Report | UC Berkeley Data 102 final project — hypothesis testing and OLS regression on EPA eGRID data. |
| [LWVO Member Demographics Analysis](projects/lwvo-demographics-analysis.html) | Poster | DataGood @ Berkeley consulting project — survey + choropleth analysis for the League of Women Voters of Oakland. |
| [Odys eVTOL Revenue Strategy](projects/odys-evtol-revenue.html) | Slide Deck | Modeled airline revenue increase from integrating Odys eVTOL aircraft, using flight/catchment-airport data. |
| [Sentiment Trend Modeling of ChatGPT Tweets](projects/chatgpt-sentiment-nlp.html) | Independent project | NLP sentiment analysis of ChatGPT-related tweets over time. |

The original deliverables for the first three (notebook, written report, poster, slide deck) are
included under `projects/files/`. The full renewable-energy notebook and its own project README
live in the separate [lydiajung-ds-portfolio](https://github.com/lydiajung02/lydiajung-ds-portfolio)
repo, which this site links out to.

## Structure

```
index.html                       landing page (project list)
resume.html                      resume page (matches assets/resume.pdf)
projects/
  renewable-energy-emissions.html
  lwvo-demographics-analysis.html
  odys-evtol-revenue.html
  chatgpt-sentiment-nlp.html
  files/                         real PDFs (report, poster, deck) embedded by the pages above
assets/
  css/style.css                  shared styles + light/dark theme
  js/theme.js                    dark mode toggle
  resume.pdf
```

## Preview locally

```bash
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Publish to GitHub Pages

This repo is named `lydiajung02.github.io`, so GitHub serves it automatically at the root
domain once pushed to `main` — no Pages settings needed:

```bash
git push -u origin main
```

Site goes live at **https://lydiajung02.github.io/** within a minute or two.

## Let's Connect

- seowoo29@berkeley.edu
- [LinkedIn](https://www.linkedin.com/in/lydia-jung/)
- [GitHub](https://github.com/lydiajung02)
