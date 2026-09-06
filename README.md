# Academic homepage

A personal academic / technical website built with al-folio v1, Jekyll and GitHub Pages.

Includes About, Research / Thesis, Projects, CV, and GitHub / Contact. English content is based on the supplied undergraduate background. Unknown identity and education details are marked as placeholders; empty contact and document links are not rendered.

Start with [中文部署指南](SETUP.zh-CN.md) and [内容核对清单](CONTENT_CHECKLIST.md).

## Local preview

Install Ruby 3.3 and Node.js 22, then run:

```sh
bundle install
bundle exec jekyll serve
```

Open http://localhost:4000. This uses the actual al-folio theme. The GitHub workflow builds the same source and deploys it with GitHub Pages Actions.

## Structure

- `_config.yml`: name, site URL, language, theme and plugins.
- `_data/profile.yml`: education, GitHub, email and optional PDF paths.
- `_pages/`: About, Research, project index, CV and Contact.
- `_projects/`: one Markdown file per project; add source links in `repository_url`.
- `_bibliography/papers.bib`: empty, ready for verified publications.
- `.github/workflows/deploy.yml`: build on pushes and pull requests; deploy main.

Upstream source and licensing are documented in [SOURCE.md](SOURCE.md).
