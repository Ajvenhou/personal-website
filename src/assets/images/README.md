# Image organization

- `site/profile/` contains profile photographs and other personal identity images used by the site.
- `site/homepage/` contains images used specifically on the homepage.
- `site/shared/` contains general website images reused across multiple pages or sections.
- `blog/` should contain a separate subfolder for each blog post when images are added.
- `projects/` should contain a separate subfolder for each research project when images are added.

Use lowercase, descriptive, hyphen-separated filenames, for example `zugspitze-summit-view.jpg`.

Astro-managed images should normally stay under `src/assets` so Astro can process and optimize them.
Files that need fixed, directly addressable URLs should go under `public/` instead.
