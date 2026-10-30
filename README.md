# Yuzhang Zhao · personal site and blog

Source for https://zhao-yz.github.io/ , built with [Hugo](https://gohugo.io/) and the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme, deployed by GitHub Actions on every push to `main`.

English is the default language at the site root; Chinese lives under `/zh/`. The language switch in the header links the two home pages.

## Layout

| Path | What it is |
| --- | --- |
| `hugo.yaml` | Site config: languages, home intro, menus, social links |
| `content/posts/` | Posts. `<slug>.md` is English, `<slug>.zh.md` is Chinese; the same slug in both languages links them as translations |
| `content/about.md`, `content/about.zh.md` | About page in each language |
| `layouts/list.html` | Overrides the theme's list page: blue title, date, one or two sentence description; also lists posts from the other language when they have no translation |
| `assets/css/extended/custom.css` | Style overrides for the list above |
| `themes/PaperMod` | Theme, a git submodule pinned to one commit |
| `.github/workflows/hugo.yaml` | Build and deploy; pins the Hugo version |

## Publish a new post

1. Create `content/posts/<slug>.zh.md` (Chinese) or `content/posts/<slug>.md` (English). The slug becomes the URL, so keep it short, lowercase and hyphenated.
2. Front matter:

   ```yaml
   ---
   title: "Post title"
   date: 2026-10-29
   description: "One or two sentences. This is the hook shown under the title in post lists."
   ---
   ```

   `date` is the publish date. Hugo skips posts dated in the future, so do not put a time later than now.
3. Preview locally with `hugo server` and open http://localhost:1313/ (Chinese pages are under `/zh/`).
4. Commit and push to `main`. The Actions run takes about a minute; check it under the repository's Actions tab.

## Setup on a new machine

```sh
git clone --recurse-submodules https://github.com/Zhao-yz/Zhao-yz.github.io.git
```

If the repo was cloned without submodules, run `git submodule update --init`. Install Hugo extended (`winget install Hugo.Hugo.Extended` on Windows, `brew install hugo` on macOS); the version used in CI is in `.github/workflows/hugo.yaml`.

## Update the theme

```sh
git submodule update --remote themes/PaperMod
hugo server
```

Check the home page, a post and the About page in both languages, since `layouts/list.html` overrides a theme template. Then commit the new submodule commit.
