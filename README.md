# MathBooks

A simple public list of math books.

## What This Repo Is

This repository is intentionally minimal:

- `CATALOG.md`: the main list of books
- `books/`: optional notes files (only if needed)
- `legacy/`: previous advanced structure (kept for reference)

## How To Add a Book (2 steps)

1. Open `CATALOG.md`.
2. Add one row to the table.

That is all.

## Catalog Format

Each row has:

- `Title`
- `Author`
- `Level` (`Beginner`, `Intermediate`, `Advanced`)
- `Topic`
- `Language` (like `EN`, `PT`, `ES`)
- `Link` (legal source)
- `Notes` (optional link to a file in `books/`)

## Legal Rule

Only include legal links or public-domain/open-access files.

## Optional Notes File

If you want personal notes for a book, create a file in `books/`:

```text
books/<short-book-name>.md
```

Example:

```text
books/linear-algebra-done-right.md
```

## Quick Start

```bash
git clone https://github.com/oaleffemanuel/mathbooks.git
cd mathbooks
```
