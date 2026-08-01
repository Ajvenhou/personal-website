# Ivo S. Vinklárek — Personal Academic Website

Source code for the personal academic website of Ivo S. Vinklárek. The site is a long-term
academic portfolio for research, projects, publications, professional information, and personal
writing.

## Technology

- [Astro](https://astro.build/) 7
- Markdown content collections
- Static HTML output
- Plain CSS and minimal client-side JavaScript
- No external UI libraries

## Current site structure

The homepage is a single academic-style page with a centered content column, sticky desktop
sidebar, compact mobile navigation, and scroll-based active-section highlighting.

Homepage sections appear in this order:

1. Welcome
2. About
3. Research
4. Projects
5. Curriculum Vitae
6. Publication List
7. Blog
8. Links
9. Contact

The Curriculum Vitae section uses a native expandable control and is closed by default. The
Publication List is an independent, always-visible section. Blog entries are listed on the
homepage and at `/blog/`, with individual static pages generated at `/blog/[id]/`.

## Content

Content collections are configured in `src/content.config.ts`:

- `src/content/*.md` contains the main homepage content.
- `src/content/blog/` contains individual blog posts.
- `src/content/projects/` contains research project entries.
- `src/content/publications/` contains publication content.

Blog and project entries can use `draft: true` in their frontmatter. Draft entries are currently
visible and marked as drafts or works in progress.

## Images

Astro-managed images live under `src/assets/images/`:

```text
src/assets/images/
├── site/
│   ├── profile/
│   ├── homepage/
│   └── shared/
├── blog/
└── projects/
```

Each blog post and research project should receive its own image subfolder when needed. See
`src/assets/images/README.md` for naming and placement guidance. Static files that require fixed,
direct URLs belong under `public/`.

## Project structure

```text
/
├── public/                 # Directly served static files
├── src/
│   ├── assets/             # Astro-managed assets and images
│   ├── content/            # Markdown content
│   ├── content.config.ts   # Content collection definitions
│   ├── layouts/
│   │   └── Layout.astro
│   └── pages/
│       ├── index.astro
│       └── blog/
│           ├── index.astro
│           └── [id].astro
├── astro.config.mjs
└── package.json
```

## Development

Install dependencies:

```sh
npm install
```

Start Astro in background mode and open the URL it reports, normally
`http://localhost:4321`:

```sh
npx astro dev --background
```

Manage the background server with:

```sh
npx astro dev status
npx astro dev logs
npx astro dev stop
```

Run only one development server for this project at a time.

Build the static production site into `dist/`:

```sh
npm run build
```

Preview a completed production build:

```sh
npm run preview
```

## Development principles

- Keep content independent from presentation.
- Prefer simple, accessible HTML and minimal JavaScript.
- Avoid unnecessary dependencies.
- Build incrementally with focused Git commits.
- Keep the site maintainable as a long-term academic portfolio.
