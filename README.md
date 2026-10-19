# Communication Theory Primer (Jekyll + GitHub Pages)

This repository hosts a Jekyll website designed for publication on GitHub Pages. It is structured for a non-technical audience and organized around communication theory lenses that can be applied to modern communication problems, including AI-related issues.

## Site structure

- `index.md` — Home page introduction
- `transmission-limits.md` — Transmission model and critique
- `meaning-and-culture.md` — Semiotic lens
- `interpretation-and-power.md` — Encoding/decoding and power
- `interpretation-and-intention.md` — Eco + *intentio algorithmi*
- `what-to-do.md` — Practical guidance page
- `how-i-built-this-site.md` — Build/process page
- `_layouts/default.html` — Shared page layout with navigation and ARIA landmarks
- `assets/css/style.css` — Royal blue design system and page styling
- `assets/images/` — Add all your images here
- `.github/workflows/jekyll.yml` — Build/deploy workflow for GitHub Pages

## Local development

1. Install Ruby and Bundler.
2. From repository root, run:
   - `bundle config set path 'vendor/bundle'`
   - `bundle install`
   - `bundle exec jekyll serve`
3. Open `http://127.0.0.1:4000/comm-primer/` in your browser.

## Publishing on GitHub Pages

The workflow in `.github/workflows/jekyll.yml` runs on every commit pushed to `main` and deploys the site to GitHub Pages.

## How to add or revise content

1. Open the page file you want to edit (`*.md` in repository root).
2. Keep the front matter keys (`layout`, `title`, `permalink`) intact.
3. Replace boilerplate text with your own analysis.
4. Use Markdown headings (`##`, `###`) to keep sections readable.
5. Add links, lists, and quotes as needed.

### Adding images

1. Place image files in `assets/images/`.
2. Reference them in Markdown using:
   - `![Descriptive alt text]({{ '/assets/images/your-image.png' | relative_url }})`
3. Always write meaningful alt text for accessibility.

## Basic site configuration

Edit `_config.yml` to update:

- `title` — Site title shown in header and metadata.
- `description` — Summary used in metadata.
- `url` — GitHub Pages root URL (`https://bryngrant.github.io`).
- `baseurl` — Repository path (`/comm-primer`).

After changing `_config.yml`, restart local server.

## Customizing the color palette and CSS variables

Open `assets/css/style.css` and edit values in `:root`:

- `--royal-900`, `--royal-700`, `--royal-500` for primary brand blues
- `--sky-100` for page background
- `--ink-900`, `--ink-700` for text tones
- `--focus` for keyboard focus outline/highlight

Keep contrast strong for accessibility when changing colors.
