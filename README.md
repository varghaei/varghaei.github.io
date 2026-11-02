# varghaei.github.io

Personal academic website of Pegah Varghaei, PhD candidate in Computer Science and Engineering at Michigan State University. Live at [varghaei.github.io](https://varghaei.github.io).

Built with [al-folio](https://github.com/alshedivat/al-folio) v1.x (Jekyll). Full al-folio documentation is in [`docs/`](docs/).

## Where things live

| What                            | File(s)                                                                   |
| ------------------------------- | ------------------------------------------------------------------------- |
| Name, site settings, features   | `_config.yml`                                                             |
| Bio, photo, contact (home page) | `_pages/about.md`, `assets/img/prof_pic.jpg`                              |
| Publications                    | `_bibliography/papers.bib`, previews in `assets/img/publication_preview/` |
| News                            | `_news/*.md` (`display_date` sets the date label shown)                   |
| Research areas                  | `_projects/*.md`, images in `assets/img/research_*`                       |
| CV page                         | `_data/cv.yml` (RenderCV format)                                          |
| Teaching and service            | `_pages/teaching.md`                                                      |
| Social links                    | `_data/socials.yml`                                                       |
| Poster and other files          | `assets/pdf/`                                                             |

`_includes/news.liquid` is a small local override of the al-folio news list: it shows a news item's `display_date` (for example `Oct 2025`) instead of a full day-level date when one is set.

## Deployment

Every push to `main` runs the **Deploy site** GitHub Action, which builds the site and publishes it to the `gh-pages` branch. In **Settings → Pages**, the source should be **Deploy from a branch → `gh-pages` / root**. In **Settings → Actions → General → Workflow permissions**, select **Read and write permissions** so the action can push to `gh-pages`.

## Local preview

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000
```

Or with Docker: `docker compose up` (see [`docs/INSTALL.md`](docs/INSTALL.md)).
