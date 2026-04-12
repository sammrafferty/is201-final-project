# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Sam Rafferty's IS-201 (BYU Marriott School, Management Information Systems) final web development project. It's a static personal site hosted on GitHub Pages at `https://sammrafferty.github.io/is201-final-project/`. There is no build system, no package manager, no test suite — just HTML, CSS, and JavaScript served as static files.

## Local development

```bash
# Start a local HTTP server (required — file:// won't run the YouTube/Tableau embeds on scratch.html)
python -m http.server 8765
# Preview at http://localhost:8765/
```

```bash
# Check GitHub Pages deployment status after pushing
gh api repos/sammrafferty/is201-final-project/pages/builds | python -c "import sys,json; b=json.load(sys.stdin)[0]; print(b['status'], b['updated_at'])"
```

Pages auto-rebuilds on every push to `main` (~60–90s latency).

## File responsibilities and architectural rules

The rubric imposes hard constraints — future edits must respect these or the grade drops. See `scratch.html` for the enforced rules.

| File | Purpose | Hard rule |
|---|---|---|
| `index.html` | Bootstrap résumé page (Start Bootstrap "Resume" theme) | Résumé must stay in HTML — **never** replace with a PDF/Google Doc link |
| `projects.html` | Second Bootstrap page showing project cards | Uses same theme CSS for consistency |
| `scratch.html` | From-scratch page (the Canvas submission URL) | **NO Bootstrap anywhere** — no bootstrap CSS link, no `container-fluid`, no `navbar-expand-*`, no `row`/`col-*`. The graders check this. |
| `app.html` | Finance Wordle web app (AI-assisted project requirement) | **Must be single-file** — all CSS inline in `<style>`, all JS inline in `<script>`. External CDN is fine. No separate `.css` or `.js` files for app.html. |
| `css/resume.css` | Start Bootstrap "Resume" theme CSS | Do not modify — it's the downloaded theme. Override via `custom.css` instead. |
| `css/custom.css` | My overrides for the Bootstrap pages (diagram's "Custom CSS 1") | Linked from `index.html` and `projects.html` after `resume.css`. |
| `css/scratch.css` | From-scratch stylesheet for `scratch.html` (diagram's "Custom CSS 2") | Rubric requires ≥4 style blocks, at least one `color:`, one `font-family:`, and ≥3 selectors using `position:`. Do not drop below those thresholds. |
| `js/scripts.js` | Start Bootstrap "Resume" theme JS | Do not modify. |

## Rubric-critical elements on scratch.html

If you edit `scratch.html`, preserve these — each is worth points:

- Nested `<ol>` containing `<ul>` ("Favorite Rides" section — 3 rides, each with a nested bullet list)
- Non-Bootstrap `<img>` (`images/mt-washington.jpg` in sidebar)
- YouTube `<iframe>` with `src="https://www.youtube.com/embed/..."`
- On-page anchors: TOC links `#rides`, `#video`, `#tableau`, `#app-link` targeting matching `id` attributes
- Custom `background-color` in `scratch.css` (`#f4ecd8`)
- Tableau live embed using the `tableauPlaceholder` div + `viz_v1.js` pattern (the existing viz is datapony's "Tour de France Dashboard" — `TourdeFranceDashboard/Dashboard2`). **Not** a static `<img>` of a chart.
- Footer nav links to `index.html`, `projects.html`, and `app.html` — all three are required per Canvas submission instructions.

## Knowledge graph

This project is indexed in graphify. When you need to understand relationships between files or concepts, prefer:

```bash
/graphify query "your question"
```

over reading raw files. A post-commit hook at `.git/hooks/post-commit` runs `graphify --update` automatically so the graph stays fresh on every commit.
