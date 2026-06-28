# Cenaculum

Website for **Cenaculum**, an immersive Latin retreat, and the **Family of Saint Jerome**.

## Tech

- **Jekyll** site deployed on **GitHub Pages**.
- All content is **Markdown** (`.md`) and styled with a single CSS file.

## Structure

```
_config.yml          # Jekyll config
_layouts/default.html # Base HTML layout that links common.css
index.md             # Home page
common.css           # All styling
pages/
  family-saint-jerome.md   # Sub-page about the Family of Saint Jerome
```

## Content conventions

- Jekyll only processes Markdown files that include YAML front matter.
- `index.md` and files in `pages/` should start with `---` and `layout: default`.
- The shared layout lives in `_layouts/default.html` and links `common.css` with `relative_url`.
- The home page lives in `index.md`. Sections are delimited by `##` headings and `---` rules.
- Sub-pages go under `pages/`.
- All CSS is in `common.css`. Uses custom properties (colors, spacing, shadows) for consistency.
- Responsive breakpoints at 900px and 650px.
- Icons are rendered as plain unicode/emoji text (no icon library).

## Adding a new page

1. Create a `.md` file in `pages/` or at the root.
2. Add front matter at the top:

   ```yaml
   ---
   layout: default
   ---
   ```

3. Add a navigation link in `index.md` if needed.
4. Style any new elements in `common.css` following existing patterns.

## Local development

```bash
# Install Jekyll and dependencies (if not already present)
gem install jekyll bundler

# Serve locally
jekyll serve
```

## Deployment

Push to the publishing branch configured in GitHub Pages. No custom workflow is needed for the basic Pages integration.
