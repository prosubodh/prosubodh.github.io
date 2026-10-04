# prosubodh.github.io

Personal portfolio and resume site of **Subodh Khanal** — Full Stack Developer & Tech Lead, remote from Kathmandu, Nepal.

Live at [prosubodh.github.io](https://prosubodh.github.io/) (GitHub Pages, served from `main`).

## Pages

| File | Description |
|---|---|
| `index.html` | Portfolio: hero, stats, about, career timeline, recommendations, projects, learning, services + rates, contact |
| `resume.html` | Printable resume with a Print / Save PDF action |
| `404.html` | Themed not-found page (`noindex`) |
| `style.css` | Single shared stylesheet, dark theme default with light theme via `light-theme` class |

## Preview locally

Any static server works, e.g. from the repo root:

```powershell
python -m http.server 8000
```

then open <http://localhost:8000>. (Use a server rather than `file://` so relative links, PDFs under `certificates/`, and screenshots resolve correctly.)

To export the resume as PDF, open `resume.html` and use the Print / Save PDF button — the print stylesheet hides chrome and keeps each role on one page.

## Assets

- `images/photo.jpg` — hero portrait (800px max, progressive JPEG)
- `images/projects/` — project screenshots (`.jpg`, 1200px max) and hand-drawn SVG placeholders
- `images/recommenders/` — testimonial photos
- `images/favicon.svg` / `images/favicon-light.svg` — dark/light tab icons
- `certificates/` — HIPAA and US Healthcare PDFs linked from Learning
- `contact.vcf` — downloadable vCard, update alongside contact details

## Contributing workflow

- Branch pattern enforced by CI: `users/<firstname>.<lastname>/<feat|fix|docs|style|refactor|test|chore>/<task-name>`
- Commit messages must start uppercase and not end with a period
- Open a PR with a description (15+ words recommended) — the **Lint PR** workflow validates branch, commits, and description
- Workflow fixes go directly to `main` first (the lint workflow runs from the base branch, so PRs can't fix it themselves)

## Notes

- No build step, no frameworks — vanilla HTML, CSS, and JavaScript plus Google Fonts
- Theme preference (`system`/`light`/`dark`) persists in `localStorage` and follows the OS setting
- `robots.txt` + `sitemap.xml` included; update `lastmod` when publishing content changes
