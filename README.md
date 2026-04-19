# Math Books Library

Public, organized, and searchable library for math books.

## Goal

This repository is a **universal catalog system** for math books.  
It is designed so anyone can add books in the same format, browse by topic, and find resources quickly.

## Important Legal Note

Only add content you are legally allowed to share.

- Prefer public-domain books (for example: Project Gutenberg, Internet Archive public items).
- For copyrighted books, store metadata + external links only.
- Do not upload pirated files.

## Universal Organization Standard

Every book gets one folder inside `books/`:

```text
books/
  <book-id>/
    metadata.yaml
    notes.md
    links.md
```

Where `<book-id>` is:

```text
<author-lastname>-<short-title>-<year>
```

Example:

```text
books/axler-linear-algebra-done-right-2015/
```

## Repository Structure

```text
math-books-library/
  README.md
  LICENSE
  books/
    <book-id>/
      metadata.yaml
      notes.md
      links.md
  indexes/
    by-topic.md
    by-level.md
    by-language.md
    by-author.md
  templates/
    metadata.template.yaml
    notes.template.md
    links.template.md
  docs/
    taxonomy.md
```

## Required Metadata Fields

Each `metadata.yaml` should contain:

- `id`: unique slug (`author-title-year`)
- `title`
- `author`
- `year`
- `language`
- `level`: `beginner | intermediate | advanced | research`
- `topics`: list using controlled taxonomy (see `docs/taxonomy.md`)
- `keywords`: free tags
- `license`: `public_domain | open_access | copyrighted`
- `availability`: `full_text | preview | metadata_only`
- `sources`: links to official/legal sources

Example:

```yaml
id: courante-differential-and-integral-calculus-vol1-1934
title: Differential and Integral Calculus, Vol. 1
author: Richard Courant
year: 1934
language: en
level: intermediate
topics:
  - calculus
  - analysis
keywords:
  - single-variable
  - classic
license: copyrighted
availability: metadata_only
sources:
  - https://archive.org/details/in.ernet.dli.2015.133025
```

## Controlled Taxonomy (Topics)

Use these main topics to keep organization universal:

- arithmetic
- algebra
- linear-algebra
- geometry
- trigonometry
- calculus
- analysis
- differential-equations
- discrete-math
- combinatorics
- number-theory
- probability
- statistics
- logic
- set-theory
- topology
- abstract-algebra
- real-analysis
- complex-analysis
- numerical-analysis
- optimization
- dynamical-systems
- game-theory
- category-theory
- foundations
- math-history
- math-education

## How To Add a Book

1. Create a folder in `books/` with the `<book-id>` format.
2. Copy templates from `templates/`.
3. Fill `metadata.yaml` completely.
4. Add learning notes in `notes.md` (optional but recommended).
5. Add legal source links in `links.md`.
6. Update one or more index files in `indexes/`.

## Index Rules

- `indexes/by-topic.md`: grouped by canonical topic names.
- `indexes/by-level.md`: grouped by learning level.
- `indexes/by-language.md`: grouped by ISO language code.
- `indexes/by-author.md`: alphabetic by author surname.

Each index entry should use this format:

```markdown
- **Title** (Year) — Author  
  ID: `book-id`  
  Topics: topic1, topic2  
  Availability: full_text | preview | metadata_only
```

## Suggested Contribution Workflow

1. Fork repository.
2. Add or update book folders.
3. Run a quick consistency check:
   - valid folder naming
   - required metadata fields present
   - taxonomy topics valid
4. Open pull request with summary of added books.

## Optional Automation Ideas

- Add a script to validate YAML metadata.
- Generate indexes automatically from `books/*/metadata.yaml`.
- Add GitHub Action to fail PRs with invalid metadata.

## Quick Start

After creating this repo on GitHub:

```bash
git clone https://github.com/<your-username>/math-books-library.git
cd math-books-library
```

Then add your first book from the templates.

## License Recommendation

Use `CC BY 4.0` for repository metadata and notes.

