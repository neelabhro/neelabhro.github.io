# Website Update Guide

This website is a lightweight static site for GitHub Pages. It does not require Jekyll, Ruby, or a build step.

## Main structure

- `index.html` is the landing page with a concise bio, current research themes, latest news, selected publications, and academic path.
- `research.html` contains research themes and selected open-source projects.
- `publications.html` contains the full selected publications list.
- `experience.html` contains research/professional experience and education.
- `news.html` contains the full news archive.
- `contact.html` contains email and profile links.
- `404.html` is the GitHub Pages not-found page.
- `static/css/site.css` contains the shared visual design.
- `static/img/` contains the profile photo and institution logos used by the site.

## How to preview locally

From the repository root, run:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## How to update content

Edit the page that owns the content:

- Bio and landing-page summaries: `index.html`
- Research themes or project cards: `research.html`
- Publications: `publications.html`
- Roles and education: `experience.html`
- News items: `news.html`
- Contact links: `contact.html`

Keep the landing page selective. Add detailed entries to the relevant subpage, and surface only the newest or most representative items on `index.html`.

## How to publish

Commit and push changes to the GitHub Pages publishing branch:

```bash
git add .
git commit -m "Refresh personal website"
git push
```
