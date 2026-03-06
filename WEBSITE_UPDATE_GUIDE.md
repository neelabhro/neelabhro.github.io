# Website Update Guide

This website is a lightweight static site intended to work well with GitHub Pages.

## Main structure

- `index.html` controls the overall page layout, navigation bar, styling, and section loading.
- `templates/about.html` contains the hero/about section.
- `templates/news.html` contains the news section.
- `templates/publications.html` contains the selected publications list.
- `templates/projects.html` contains the selected projects cards.
- `templates/experience.html` contains research/professional experience.
- `templates/education.html` contains education entries.
- `templates/achievements.html` contains highlights.
- `templates/contact.html` contains contact details.
- `static/img/` contains profile photos and other image assets.
- `static/docs/` can contain your CV, slides, PDFs, or other downloadable documents.

## How to edit content

### 1. Update bio and profile links
Edit:
- `templates/about.html`
- `templates/contact.html`

### 2. Update publications
Edit:
- `templates/publications.html`

Recommended pattern for a publication block:

```html
<div class="pub-item">
  <div class="meta">Conference paper · 2026</div>
  <div><b>Paper title</b><br>
  Author list<br>
  <i>Venue</i><br>
  <a target="_blank" href="LINK">Link</a></div>
</div>
```

### 3. Update projects
Edit:
- `templates/projects.html`

Each project is a Bootstrap card-style block using the `card-lite` class.

### 4. Update styling
Edit:
- `index.html`

Most visual styling lives inside the `<style>` block in `index.html`.
Useful classes include:
- `.section-shell`
- `.hero`
- `.card-lite`
- `.pub-item`
- `.timeline-item`
- `.btn-soft`
- `.pill`

### 5. Update images
Put new assets into:
- `static/img/`

Then reference them like:

```html
<img src="/static/img/your-image-name.png" alt="Description">
```

## How to preview locally

### Option A: simple Python server
From the repository root, run:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

### Option B: GitHub Pages workflow
If this repository is already connected to GitHub Pages, pushing changes to the default publishing branch should update the site automatically.

## How to publish updates on GitHub

1. Unzip the folder.
2. Replace or edit the relevant files.
3. Commit the changes.
4. Push the repository to GitHub.
5. Wait for GitHub Pages to redeploy the site.

Typical commands:

```bash
git add .
git commit -m "Refresh website content and publications"
git push
```

## Suggested ongoing workflow

- Keep `templates/publications.html` as a curated selected-publications list.
- Add a Scholar link for the full publication record.
- Update `news.html` only for major milestones.
- Keep `projects.html` focused on systems and software artifacts rather than every paper.

