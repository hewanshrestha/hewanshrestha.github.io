# hewanshrestha.github.io

Personal academic website of Hewan Shrestha, served by GitHub Pages at
<https://hewanshrestha.github.io>.

A single static page — no build step.

```
index.html        intro, experience timeline, research interests, news, publications
404.html          not-found page
css/styles.css    site styles (the Bootstrap grid and FontAwesome sit alongside it)
images/           portrait, institution logos, publication thumbnails
files/            CV and papers
robots.txt
sitemap.xml
```

## Editing

- **News** — add a `<div class="news-item">` at the top of `.news-scroll`, with a
  `<span class="news-date">` and a `<p>`. The panel is a fixed-height scroll box
  (`max-height` in `.news-scroll`), so new items need no other change.
- **Publications** — only selected papers are listed here; everything else is behind
  the Google Scholar link in `.pub-more`. Copy an existing `.row.publication` block
  to add one, using `col-lg-4` + `col-lg-8` with a thumbnail or a single `col-lg-12`
  without.
- **Research interests** — four `.interest-box` cards in a `.interest-grid`; the grid
  drops to one column under 768px.
- **Experience** — each timeline entry is an `<li>` with a `.logo` image and a
  `.description`. Logos share one fixed box (`li .logo`, 132x58) with
  `object-fit: contain`, so wide lock-ups and square marks both read clearly; no
  per-logo `transform: scale()` needed.

Preview locally:

```bash
python3 -m http.server 8000
```
