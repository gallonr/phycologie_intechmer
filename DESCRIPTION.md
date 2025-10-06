# Phycologie Intechmer — Bookdown Project

## Project Overview

This repository contains a Bookdown project for a French-language educational book on marine plant biology taught at Cnam–Intechmer. It compiles R Markdown chapters into a multi-format book (HTML/PDF/EPUB) with cross-references, bibliography, and responsive styling.

- Language: French
- Author: Régis GALLON
- Institution: Cnam–Intechmer
- Primary output: HTML site (GitHub Pages via `docs/`)
- Last reviewed: 2025-10-06

## Tech Stack

- R Markdown (authoring)
- Bookdown (book generation)
- GitBook theme for HTML
- LaTeX (PDF via `preamble.tex`)
- KaTeX/MathJax for math rendering

## Key Features

- Multi-format output: HTML, PDF (and EPUB artifacts in `_book/`)
- Searchable HTML (client-side search index)
- Cross-references (figures, tables, sections)
- Bibliography with BibTeX (`book.bib`, `biblio/refs.bib`)
- Custom styling via `style.css`

## Repository Layout

### Core configuration
- `_bookdown.yml` — Bookdown configuration (files order, repo settings)
- `_output.yml` — Output format and theme settings
- `preamble.tex` — LaTeX preamble for PDF builds
- `style.css` — Custom CSS applied to HTML outputs
- `book.bib`, `packages.bib` — Bibliography sources

### Chapters (Rmd)
1. `01-histoire.Rmd` — Histoire de l'utilisation des algues
2. `02-usage.Rmd` — Usages, économie et règlementation
3. `03-classif.Rmd` — Classification et diversité
4. `04-morphologie.Rmd` — Diversité morphologique des algues
5. `05-cytologie.Rmd` — Diversité cytologique
6. `06-biochimie.Rmd` — Biochimie associée aux algues
7. `20-glossaire.Rmd` — Glossaire
8. `21-references.Rmd` — Références

### Outputs
- `docs/` — Published HTML site (entry point `docs/index.html`), suitable for GitHub Pages
- `_book/` — Build artifacts (HTML, PDF, EPUB, TeX), typically not published
- `_bookdown_files/` — Cache and intermediates for faster builds

### Assets and data
- `images/` — Image assets used throughout the book
- `data/` — Data files referenced in chapters
- `biblio/` — Additional bibliography resources (e.g., `refs.bib`)

### Meta and tooling
- `README.md` — Minimal description and getting-started notes
- `LICENSE` — Project license
- `phycology_book.Rproj` — RStudio project
- `.github/workflows/bookdown.yml` — (If present) CI for building and/or deploying

## Build & Publish

- Local builds typically render to `_book/`.
- GitHub Pages is served from `docs/` in this repository; HTML outputs are mirrored there for publishing.
- The workflow file in `.github/workflows/bookdown.yml` (if enabled) can automate rendering and deployment to `docs/`.

## Notable HTML pages in `docs/`

- `docs/index.html` — Landing page
- `docs/histoire.html`, `docs/usage.html`, `docs/classification.html`, `docs/morphologie.html`, `docs/cytologie.html`, `docs/biochimie.html`
- `docs/glossaire.html`, `docs/références.html`
- `docs/404.html` — Custom error page

## Notes

- Some outputs in `_book/` include `phycology_book.pdf`, `phycology_book.epub`, and the generated TeX file.
- The project name, chapter order, and output formats are controlled by `_bookdown.yml` and `_output.yml`.
- Ensure images referenced in chapters exist under `images/` with correct paths.
