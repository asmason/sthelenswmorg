# AGENTS.md

Static HTML website for St. Helen's Church, Welton. No build step, no package manager, no server code — pages are plain HTML opened directly in a browser.

## Repo layout (important)

- The git repo and all site content live in the `sthelenswmorg/` **subdirectory** of the outer workspace folder. The outer folder is NOT a repo. Run all `git` commands from `sthelenswmorg/`.
- Deployed to GitHub Pages at `sthelenswm.org` via `CNAME`; pushing to `main` publishes the site.

## Working with pages

- Every page duplicates the **full navbar and footer nav** inline (no includes/templating). When adding, renaming, or removing a page, update the nav in **every** `.html` file plus `sitemap.xml` and `robots.txt` (sitemap URL).
- Bootstrap 5.0.2 and jQuery 3.7.1 are loaded from CDN. Only `styles.css` holds custom CSS.
- `index.html` is the main routine-maintenance file: it holds a chronological list of dated "upcoming services" cards. Add/remove cards in date order and update the trailing `Last updated:` line.
- `sitemap.xml` lists every page — keep it in sync when pages change.
- `index-bak.bak` is a stale leftover backup; don't treat it as canonical.

## Verification

- No lint/test/typecheck. Verify by opening the affected `.html` in a browser and confirming links/image paths are relative and correct.
- Commit style is short, e.g. "Update index.html".