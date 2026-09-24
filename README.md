# Yuzhang (Ernie) Zhao — Portfolio

This is a static Jekyll site for GitHub Pages. The published website is built directly from the repository root; it does not need a separate app, backend, or manual build workflow on GitHub.

## Update the site

- Edit `index.md`, `about.md`, `experience.md`, or `contact.md` to update page content. Each page has YAML front matter at the top for its title, description, and URL.
- Edit `_config.yml` to update the site title, description, contact links, or navigation.
- Shared HTML lives in `_layouts/default.html` and `_includes/`. Styles are in `assets/css/main.css`; the favicon is `assets/favicon.svg`.
- Keep personal claims and metrics factual and supplied by Yuzhang. Do not add a phone number unless requested.

## Preview locally

Install Ruby and Bundler if they are not already installed, then run:

```sh
bundle install
bundle exec jekyll serve
```

Open <http://127.0.0.1:4000>. Jekyll regenerates the local preview when you edit site files. The local server is only for previewing; GitHub Pages publishes the static site.

To generate the static output locally instead:

```sh
bundle exec jekyll build
```

Jekyll writes build output to `_site/`. Do not commit that generated directory.

## Publish with GitHub Pages

1. Use the GitHub user-site repository named `Zhao-yz.github.io`.
2. Push this repository’s contents to the `main` branch.
3. In the repository’s **Settings → Pages**, select **Deploy from a branch**, choose `main`, and choose `/(root)`.
4. Save. GitHub Pages will build this Jekyll site from the repository root. Keep `baseurl` empty in `_config.yml` for the user-site domain.

The site uses GitHub Pages-supported `jekyll-seo-tag` and `jekyll-sitemap` plugins. Internal page links, the stylesheet, the favicon, and the sitemap URL use Jekyll URL filters.

## Run Lighthouse

1. Preview locally with `bundle exec jekyll serve`, or open the published GitHub Pages URL.
2. In current desktop Google Chrome, open the page and open Developer Tools.
3. Select the **Lighthouse** panel, choose **Mobile** or **Desktop**, and generate a report.
4. Check Performance, Accessibility, Best Practices, and SEO. The target for each category is at least 90.

Run the report on the home page and at least one content page. The site avoids external fonts, trackers, frameworks, and client-side JavaScript to keep the pages lightweight.