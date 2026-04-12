# Graph Report - C:/Users/sammr/Desktop/is201-final-project  (2026-04-11)

## Corpus Check
- 5 files · ~73,832 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 35 nodes · 37 edges · 9 communities detected
- Extraction: 76% EXTRACTED · 24% INFERRED · 0% AMBIGUOUS · INFERRED: 9 edges (avg confidence: 0.79)
- Token cost: 0 input · 0 output

## God Nodes (most connected - your core abstractions)
1. `Rubric-Critical Elements on scratch.html` - 9 edges
2. `File Responsibilities and Architectural Rules` - 7 edges
3. `Sam Rafferty Cycling at Mt Washington (Race Action Shot)` - 5 edges
4. `Start Bootstrap Resume Theme v7.0.6` - 4 edges
5. `Bootstrap ScrollSpy Initialization` - 3 edges
6. `Responsive Navbar Auto-Collapse` - 3 edges
7. `Tableau Live Embed (TourdeFranceDashboard/Dashboard2)` - 3 edges
8. `Cycling Theme of scratch.html` - 3 edges
9. `index.html Rule: Resume Must Stay HTML` - 2 edges
10. `scratch.html No-Bootstrap Rule` - 2 edges

## Surprising Connections (you probably didn't know these)
- `README Pages List` --semantically_similar_to--> `File Responsibilities and Architectural Rules`  [INFERRED] [semantically similar]
  README.md → CLAUDE.md
- `resume.css Do-Not-Modify Rule` --rationale_for--> `Start Bootstrap Resume Theme v7.0.6`  [INFERRED]
  CLAUDE.md → js/scripts.js
- `Non-Bootstrap img (mt-washington.jpg) Requirement` --references--> `Sam Rafferty Cycling at Mt Washington (Race Action Shot)`  [EXTRACTED]
  CLAUDE.md → images/mt-washington.jpg
- `Sam Rafferty Cycling at Mt Washington (Race Action Shot)` --conceptually_related_to--> `Tableau Live Embed (TourdeFranceDashboard/Dashboard2)`  [INFERRED]
  images/mt-washington.jpg → CLAUDE.md
- `Sam Rafferty Cycling at Mt Washington (Race Action Shot)` --references--> `Sam Rafferty (Student/Author)`  [EXTRACTED]
  images/mt-washington.jpg → README.md

## Hyperedges (group relationships)
- **scratch.html Rubric Requirements Bundle** — claudemd_scratch_no_bootstrap, claudemd_nested_ol_ul, claudemd_non_bootstrap_img, claudemd_youtube_iframe_req, claudemd_anchor_links_req, claudemd_bg_color_req, claudemd_tableau_embed_req, claudemd_footer_nav_req, claudemd_scratch_css_thresholds [EXTRACTED 0.95]
- **Start Bootstrap Theme Lockdown (Do-Not-Modify Files)** — scripts_startbootstrap_theme, claudemd_resume_css_dont_modify, claudemd_scripts_js_dont_modify [EXTRACTED 0.90]
- **Sam Rafferty Personal Identity (Professional + Cycling)** — concept_sam_rafferty, img_headshot_sam, img_mt_washington_cycling, concept_cycling_theme [INFERRED 0.85]

## Communities

### Community 0 - "Bootstrap Theme"
Cohesion: 0.33
Nodes (7): resume.css Do-Not-Modify Rule, scripts.js Do-Not-Modify Rule, Responsive Navbar Auto-Collapse, #navbarResponsive DOM Target, Bootstrap ScrollSpy Initialization, #sideNav DOM Target, Start Bootstrap Resume Theme v7.0.6

### Community 1 - "Scratch Page Content"
Cohesion: 0.38
Nodes (7): Nested ol/ul Favorite Rides Requirement, Non-Bootstrap img (mt-washington.jpg) Requirement, Tableau Live Embed (TourdeFranceDashboard/Dashboard2), Cycling Theme of scratch.html, Sam Rafferty (Student/Author), Sam Rafferty Professional Headshot, Sam Rafferty Cycling at Mt Washington (Race Action Shot)

### Community 2 - "File Rules and Architecture"
Cohesion: 0.33
Nodes (7): app.html Single-File Rule, File Responsibilities and Architectural Rules, index.html Rule: Resume Must Stay HTML, scratch.css Rubric Thresholds (4 blocks, color, font-family, 3 position selectors), scratch.html No-Bootstrap Rule, Finance Wordle (AI-collaborated app), README Pages List

### Community 3 - "Rubric Elements"
Cohesion: 0.4
Nodes (5): On-Page Anchor Links (#rides, #video, #tableau, #app-link), Custom background-color #f4ecd8, Footer Nav Links to index/projects/app, Rubric-Critical Elements on scratch.html, YouTube iframe Embed Requirement

### Community 4 - "Local Dev Setup"
Cohesion: 1.0
Nodes (2): Local HTTP Server Requirement (python -m http.server 8765), No Build System Constraint

### Community 5 - "Graphify Integration"
Cohesion: 1.0
Nodes (2): Graphify Knowledge Graph Integration, Post-Commit Hook for graphify --update

### Community 6 - "Project Overview"
Cohesion: 1.0
Nodes (2): IS-201 Final Project Overview, IS 201 Final Project - Sam Rafferty

### Community 7 - "Deployment"
Cohesion: 1.0
Nodes (2): GitHub Pages Deployment, GitHub Pages Hosted URL

### Community 8 - "Theme JS"
Cohesion: 1.0
Nodes (0): 

## Knowledge Gaps
- **15 isolated node(s):** `#sideNav DOM Target`, `#navbarResponsive DOM Target`, `IS-201 Final Project Overview`, `No Build System Constraint`, `Local HTTP Server Requirement (python -m http.server 8765)` (+10 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **Thin community `Local Dev Setup`** (2 nodes): `Local HTTP Server Requirement (python -m http.server 8765)`, `No Build System Constraint`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Graphify Integration`** (2 nodes): `Graphify Knowledge Graph Integration`, `Post-Commit Hook for graphify --update`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Project Overview`** (2 nodes): `IS-201 Final Project Overview`, `IS 201 Final Project - Sam Rafferty`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Deployment`** (2 nodes): `GitHub Pages Deployment`, `GitHub Pages Hosted URL`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Theme JS`** (1 nodes): `scripts.js`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Rubric-Critical Elements on scratch.html` connect `Rubric Elements` to `Scratch Page Content`, `File Rules and Architecture`?**
  _High betweenness centrality (0.340) - this node is a cross-community bridge._
- **Why does `File Responsibilities and Architectural Rules` connect `File Rules and Architecture` to `Bootstrap Theme`?**
  _High betweenness centrality (0.333) - this node is a cross-community bridge._
- **Are the 2 inferred relationships involving `Sam Rafferty Cycling at Mt Washington (Race Action Shot)` (e.g. with `Tableau Live Embed (TourdeFranceDashboard/Dashboard2)` and `Sam Rafferty Professional Headshot`) actually correct?**
  _`Sam Rafferty Cycling at Mt Washington (Race Action Shot)` has 2 INFERRED edges - model-reasoned connections that need verification._
- **What connects `#sideNav DOM Target`, `#navbarResponsive DOM Target`, `IS-201 Final Project Overview` to the rest of the system?**
  _15 weakly-connected nodes found - possible documentation gaps or missing edges._