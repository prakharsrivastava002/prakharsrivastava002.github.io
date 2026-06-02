# Prakhar Srivastava — Portfolio

Personal GitHub Pages portfolio for [Prakhar Srivastava](mailto:prakharsrivastava002@gmail.com).

Built with [Jekyll](https://jekyllrb.com/) and hosted on [GitHub Pages](https://pages.github.com/). No npm, no build frameworks, no custom plugins — works with the standard GitHub Pages Jekyll pipeline.

## Live Site

> Update this URL after deployment.
> `https://<your-github-username>.github.io`

## Structure

```
├── _config.yml              # Jekyll configuration + exclude list
├── index.md                 # Homepage (Hero · Impact · Publications · Recognition · Experience · Contact)
├── achievements.md          # Full impact metrics, grouped by employer
├── publications.md          # Publications with DOIs and verification notes
├── _layouts/
│   └── default.html         # Base HTML shell (head, nav, footer)
├── _includes/
│   ├── header.html          # Sticky nav bar
│   └── footer.html          # Footer strip
├── _data/
│   ├── profile.yml          # Name, headline, experience, education, skills
│   ├── achievements.yml     # Impact metrics (all resume-sourced)
│   ├── publications.yml     # 4 publications (all verified_public)
│   └── awards.yml           # Awards and recognition (O-1A highlighted)
├── assets/
│   └── css/style.css        # All styles — no external CSS frameworks
└── notes/
    └── source_audit.md      # Verification log (excluded from build, not published)
```

## Local Preview

Requires Ruby. Run once:

```bash
gem install jekyll bundler
```

Then from the repo root:

```bash
jekyll serve --livereload
# Open: http://localhost:4000
```

## Deployment to GitHub Pages

1. Create a new GitHub repo (e.g. `prakharsrivastava.github.io` for a root site, or any name for a project site).
2. Copy all portfolio files into the new repo and push to `main`.
3. Go to **Settings → Pages → Source**: select `main` branch, `/ (root)` → **Save**.
4. GitHub builds and deploys within ~60 seconds.
5. Set `url` in `_config.yml` to your live URL.

## Updating Content

All content lives in `_data/*.yml` — no HTML editing needed for most changes:

| What to update | File |
|---|---|
| Name, headline, skills, experience, education | `_data/profile.yml` |
| Impact metrics | `_data/achievements.yml` |
| Publications | `_data/publications.yml` |
| Awards / recognition | `_data/awards.yml` |
| Site title, base URL, exclude list | `_config.yml` |
| Design, colors, typography | `assets/css/style.css` |

## Source Audit

`notes/source_audit.md` contains the full verification log of all data sources. It is excluded from the Jekyll build via `_config.yml` and is **not published** to the live site.
