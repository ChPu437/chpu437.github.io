# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Official website for the SEU Computer Science Elite Student Training Base (东南大学计算机科学拔尖学生培养基地, class code "09J"). Static site built with Jekyll, deployed via GitHub Pages to `chpu437.github.io` and production at `bj.cs.seu.edu.cn`.

## Build & Dev Commands

```bash
bundle install                  # Install Ruby dependencies
bundle exec jekyll serve        # Local dev server (http://localhost:4000)
bundle exec jekyll build        # Build site to _site/
./prepare_webplus_zip.sh        # Build + package for WebPlus CMS deployment
```

## Architecture

- **Jekyll >= 4.2.0** static site with Kramdown (GFM) markdown
- **Bootstrap 3** (vendored SCSS in `_sass/bootstrap/`) + jQuery
- **Content is data-driven:** pages pull from YAML files in `_data/` (news, students, staff, gallery photos)
- **Custom plugin:** `_plugins/markdown.rb` provides a Liquid tag for including Markdown files

### Key Directories

| Path | Purpose |
|------|---------|
| `_data/` | YAML data files — the source of truth for all dynamic content (news, team, gallery) |
| `_pages/` | Site pages (Markdown + Liquid frontmatter) |
| `_layouts/` | HTML layout templates (`homelay`, `gridlay`, `piclay`, `textlay`, `team`) |
| `_includes/` | Reusable HTML partials (header, footer, news widget) |
| `_sass/seu-custom/` | Project-specific styles (variables, components, page-scoped) |
| `images/teampic/` | Team member photos |
| `Docs/` | Contributor guides for content and style changes |

## Content Editing Patterns

- **News:** Add entry to `_data/news.yml` with `date` and `headline` fields
- **Team members:** Edit `_data/staff.yml` or `_data/students20XX.yml`, add photo to `images/teampic/`
- **Gallery:** Edit `_data/pics.yml` under `ourgroup` key, add image to `images/gallery/` (recommended 1280x960px)

## Style Rules (MUST follow)

1. **Never modify:** `css/main.scss`, `_sass/bootstrap/`, or `_sass/seu-custom/_netsi-inherited.scss`
2. Custom variables → `_sass/seu-custom/_variables.scss`
3. Page-specific styles → `_sass/seu-custom/page/_pagename.scss`
4. Component styles → `_sass/seu-custom/components/_componentname.scss`
5. New style files must be imported in `_sass/_seu-custom.scss`
6. Each page body has class `page-[slug]` for scoped styling
7. Avoid inline styles for persistent layout elements

## Branch & Workflow

- Main branch: `master`
- Contributors fork → make changes → submit PR
- Code owners defined in `.github/CODEOWNERS`
- Verify with `bundle exec jekyll serve` before submitting
