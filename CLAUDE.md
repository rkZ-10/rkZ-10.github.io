# Portfolio site

A single static page, `index.html`, served by GitHub Pages at https://rkz-10.github.io/. No build step,
no framework, no JavaScript dependencies: all CSS and the small theme script are inline in the page.
The companion blog lives at https://rkz-10.github.io/blog/ (a separate repo).

## Structure of `index.html`

- `<head>`: meta tags, including `robots: noindex, nofollow` and the Open Graph / Twitter card tags
  (`og:image` is `og-image.png`, 1200×627, referenced by absolute URL). Fonts: Spectral (headings),
  IBM Plex Sans (body), IBM Plex Mono (labels).
- Theme tokens on `:root` (`--bg`, `--surface`, `--fg`, `--muted`, `--accent`, `--accent-soft`, `--border`),
  redefined for dark mode under `prefers-color-scheme` and `[data-theme="dark"]`.
- Header (`.hero`) with name, role and the `.contact-card` rows; then sections **Stack**, **Experience**
  and **Case studies**; then the footer with `.foot-links`.
- Each case study is a `.case` block: `.case-head` (`h3` + `.case-tag`), `.case-sub`, then `.case-block`s
  with a `.k` label (Problem / Approach / Outcome), optional `.diagram` image, and `.outcome-stat` highlights.
  New case studies copy an existing one's markup exactly.

## Rules

- Reuse existing classes and tokens; don't add CSS unless asked, and never a framework or build step.
- Check every change in light mode, dark mode and at phone width (~390 px, no horizontal scroll).
- Contact details: keep the existing ones as they are and don't add new ones.
- Keep claims accurate and specific; numbers on the page must match the linked projects.
- Links to my own sites (blog) open in the same tab; external links keep `target="_blank" rel="noopener"`.
- Images: `loading="lazy"`, meaningful `alt` text, sized to the content column.
