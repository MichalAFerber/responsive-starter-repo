# Responsive Starter (Jekyll + GitHub Pages, 2025)

Ready-to-commit starter with:
- Fluid type/spacing, mobile-first breakpoints
- Container queries (progressive)
- `<picture>` + `srcset` helpers and `image-set()` backgrounds
- SVG sprite include
- GitHub Actions workflow to build and deploy to **gh-pages**

## Quick start

```bash
# local
bundle install
bundle exec jekyll serve
# then open http://127.0.0.1:4000
```

## Deploy to GitHub Pages (gh-pages)

1. Create a new GitHub repo and push these files.
2. In repo settings → **Pages**: set **Source** to "Deploy from a branch", then branch: `gh-pages`, folder: `/ (root)` — you can do this after the first deploy runs.
3. The workflow below builds to `_site/`, uploads artifact, and deploys to `gh-pages`.

### If your project is a user/org site

- Set `url:` in `_config.yml` to your domain.
- Keep `baseurl: ""`.

### If your project is a project site

- Set `url:` to `https://USERNAME.github.io`
- Set `baseurl:` to `/REPO`
- Update asset links if needed to use `{{ '/path' | relative_url }}`.

## Images

Replace `/img/...` placeholders with your own image assets.

## Security

If you accept user SVG uploads, sanitize before inlining.
