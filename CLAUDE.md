# klaine.github.io

User-level GitHub Pages site (served at https://klaine.github.io/ from the root of `main`): a gallery
of the account's projects with links to each one's pages and repository.

- One static `index.html` (inline CSS and JS, no build, no dependencies). `CATALOG` holds the
  curated entries; screenshots are `img/<repo>.jpg`, 800×500.
- `enrich()` calls the public GitHub API for update dates and for Pages repositories not in
  `CATALOG`. The page must stay complete when that request fails.
- Every project site shares this origin, so their `localStorage` is shared too: never clear it,
  remove only a page's own keys.
- Serve locally with `python3 -m http.server` from this folder.
