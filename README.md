# klaine.github.io

The account-level GitHub Pages site: a gallery of the tools and synths published under
[klaine](https://github.com/klaine), each with links to its live pages and its repository.

Live at https://klaine.github.io/.

## How it works

`index.html` is a single static page with no build step. The `CATALOG` list near the top of its
script holds the curated entries: name, description, tags, the page links, and a screenshot in
`img/<repo>.jpg`.

On load the page also asks the GitHub API for the account's public repositories. It shows each
entry's last update date, adds any repository with GitHub Pages that isn't in `CATALOG` under
"Also on GitHub Pages", and lists public repositories without Pages under "Other repositories".
The page works without that request (offline, or over the API's rate limit); it just skips those
extras.

## Adding a project

Add an entry to the right group in `CATALOG`, put a 16:10 screenshot (800×500 works) at
`img/<repo>.jpg`, and push to `main`.
