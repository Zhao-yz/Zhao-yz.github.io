# Portfolio Site Plan

## Goal

Build a personal portfolio for Yuzhang (Ernie) Zhao as a static Jekyll site published by GitHub Pages from the `main` branch and repository root at `zhao-yz.github.io`.

## Pages and content

- **Home** (`index.md`): name and supplied tagline, with clear links to the other pages.
- **About** (`about.md`): supplied MBA, engineering, product, and current AI-focus background; supplied education, skills, and certifications.
- **Work Experience** (`experience.md`): supplied TikTok, United AI, and Tsinghua Speech Recognition Lab roles and bullet points.
- **Contact** (`contact.md`): supplied public email as a `mailto:` link and supplied LinkedIn profile; no phone number.

All page copy will use Markdown and YAML front matter. No achievements, employers, clients, metrics, or projects will be invented. Any future content that has not been supplied will be identified as a placeholder.

## Design and structure

- Responsive, single-column layout with generous whitespace, clear heading hierarchy, and accessible contrast.
- Light theme only; modern professional system sans-serif with stronger heading weights.
- Semantic HTML with shared Jekyll layout and reusable navigation and footer includes.
- Plain CSS and minimal JavaScript; no backend, form, blog, CMS, animation system, tracker, or framework.

## GitHub Pages and documentation

- Root-level `_config.yml` with `url: "https://zhao-yz.github.io"` and an empty `baseurl`.
- Root-level Markdown pages, `_layouts/`, `_includes/`, and `assets/`; links and asset paths will use Jekyll URL filters.
- GitHub Pages-compatible SEO and sitemap plugins, plus a favicon.
- `README.md` with content-editing guidance, local preview steps, GitHub Pages root publishing settings, and Lighthouse instructions.
- Remove the unrelated starter applications and monorepo scaffolding so the repository root contains the complete static Jekyll site.

## Verification

- Confirm the required site files are directly in the repository root and the Pages source is `main` / root.
- Check page/navigation links, responsive layout at 375px and 1280px, and Lighthouse Performance, Accessibility, Best Practices, and SEO scores (target: at least 90 each).

## Assumptions

- The site will use the supplied email and LinkedIn URL publicly, as approved.
- The TikTok role will be presented as current, with the supplied extension through November 2026 noted.
- No profile photo or additional assets are required.