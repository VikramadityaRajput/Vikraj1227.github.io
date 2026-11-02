# Vikramaditya's Portfolio

A zero-dependency, zero-JavaScript static portfolio for Summer 2027 Software Engineering and Quantitative Development internship applications.

## Static Edge Architecture

The site is plain files, so any CDN can serve it directly from its edge locations.

```
Browser ──► CDN edge (cached HTML/CSS/PDF) ──► (rare) origin: static files
```

- **No server runtime.** There is no backend, database, or build step. `index.html` and two CSS files are served as-is.
- **Edge-cached.** Each request is answered from the nearest edge node, so first paint is fast and the site holds up under traffic spikes.
- **Small attack surface.** No server code, no secrets, no API endpoints.
- **Portable hosting.** Deploys unchanged to GitHub Pages, Cloudflare Pages, or Hostinger.
- **Progressive enhancement.** There are no polyfills and no JavaScript. Modern CSS enhances the page, and older browsers still get readable semantic HTML.

## Structure

```
index.html        Semantic page: hero, experience, projects
css/tokens.css    Design tokens (primitives and semantic)
css/styles.css    Component styles, using semantic tokens only
resume.pdf        Add your resume here (linked from the hero and footer)
```

## Design tokens and dark mode

- Primitives (`--p-*`) hold raw values such as colors, spacing, and fonts.
- Semantic tokens (`--s-*`) map primitives to roles, for example `--s-bg` and `--s-text`.
- Theming uses `color-scheme: light dark` and `light-dark()`, so the site follows the system preference. It does this in CSS alone, so it works even if JavaScript fails.
- `styles.css` references only `--s-*` tokens.

## Before deploying

1. Add `resume.pdf` to the project root.
2. Replace the placeholder `https://github.com/` and `https://www.linkedin.com/` links in `index.html` with your profile URLs.
3. Push to your static host. No build command is needed, and the publish directory is the repo root.
