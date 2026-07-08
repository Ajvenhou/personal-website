# Architecture Decisions

## 2026-07-08

## Why Astro?

Astro was chosen as the static site generator for this project because the website is content-focused and should remain simple, fast, and maintainable.

Astro supports Markdown-based content, reusable layouts, content collections, and static generation by default. This matches the goals of the website: blog posts, research projects, publications, CV, and future teaching materials.

Alternatives considered:
- Jekyll: good GitHub Pages integration, but older and Ruby-based.
- Hugo: very fast and mature, but its templating system may be less beginner-friendly.
- Eleventy: flexible and minimal, but requires more architectural decisions.
- Next.js: powerful, but more complex than needed for a mostly static personal academic site.
- Docusaurus/VitePress: excellent for documentation, but less suitable for a personal academic portfolio.

Decision: use Astro because it provides a good balance between simplicity, maintainability, modern tooling, and long-term flexibility.
---

### Why Markdown?

- Easy to write
- Version-controlled with Git
- Portable
- Future-proof

---

### Why GitHub?

- Version control
- Free hosting with GitHub Pages
- Public portfolio of the project's development