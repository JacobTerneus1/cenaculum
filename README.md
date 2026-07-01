# Cenaculum

Website for the **Cenaculum**, which is an immersive, Catholic, Latin retreat/conference hosted by the **Family of Saint Jerome**.

## Tech

- **Jekyll** site deployed on **GitHub Pages** with a custom domain: cenaculumlatinum.org
- `_site/` is generated output from Jekyll. Edit the source files, not the built copies.

## Structure

```
_config.yml              # Minimal Jekyll config
_layouts/default.html    # Shared layout, header/footer, and language-toggle script
CNAME                    # Custom domain for GitHub Pages
index.html               # Main homepage with most site content
common.css               # Shared site styling
favicon.ico              # Site favicon
pages/
  family-saint-jerome.md # Family of Saint Jerome sub-page
_site/                   # Generated site output; ignored in git and rebuilt automatically
```


## Content conventions

- Jekyll only processes files that include YAML front matter.
- `index.html` and files in `pages/` should start with `---` and `layout: default`.
- The shared layout lives in `_layouts/default.html` and links `common.css` with `relative_url`.
- The shared layout also contains the language toggle script and the site-wide header/footer.
- The home page lives in `index.html`.
- Sub-pages go under `pages/`.
- Bilingual content is written inline using paired `data-lang="eng"` and `data-lang="lat"` blocks. Keep both versions in sync when editing.
- All CSS is in `common.css`. Uses custom properties (colors, spacing, shadows) for consistency.
- Responsive breakpoints at 900px and 650px.
- Icons are rendered as plain unicode/emoji text (no icon library).
- Internal links and asset URLs should use Jekyll's `relative_url` filter in layouts/pages when appropriate.

## Adding a new page

1. Create a .md or .html file in `pages/` or at the root.
2. Add front matter at the top:


   ```yaml
   ---
   layout: default
   ---
   ```

3. Add a navigation link in `index.html` if needed.
4. Style any new elements in `common.css` following existing patterns. Prefer to use existing classes instead of creating new ones.  Prefer simple, understandable, minimal css over fancy and overbuilt.
5. If the page is bilingual, add matching English and Latin `data-lang` blocks.

## Local development

```bash
# Install Jekyll tooling globally if not already present
gem install jekyll bundler

# Serve from the repo root
jekyll serve
```

- This repo does not currently include a `Gemfile`, so `bundle exec jekyll serve` is not the default workflow here.
- Running `jekyll serve` will rebuild `_site/` locally, but those generated files should stay untracked.

## Deployment

GitHub Pages publishes from the `main` branch and runs its own Jekyll build. Commit the source files; do not commit `_site/`.

