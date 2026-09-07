# Publishing a Jupyter Book (for instructors/TAs)

This chapter is for whoever maintains this training module — it documents
how this very book was built, so it can be updated or extended later
without starting from scratch. Students do not need this chapter to
complete the course project.

## What "Jupyter Book" means today

The current Jupyter Book (v2) is built on **MyST** (`mystmd`), a
Markdown-based authoring system. A project is just a folder of Markdown
files and/or `.ipynb` notebooks, plus one configuration file,
`myst.yml`, that lists them in order.

```{admonition} Node.js required
:class: note
`jupyter-book` (v2) runs on Node.js under the hood. This container has
Node 22 and npm available; if you're setting this up somewhere new,
install Node.js first.
```

## Setting up a new book

```bash
pip install jupyter-book
mkdir my-training-book && cd my-training-book
jupyter-book init
```

`init` creates a starter `myst.yml`. Edit it to add a title, authors, and
a table of contents. A minimal example (trimmed from this book's own
config):

```yaml
version: 1
project:
  title: Creating and Publishing Jupyter Notebooks
  authors:
    - name: Guoqing Lu
  toc:
    - file: index.md
    - file: 01-what-is-a-notebook.md
    - file: 02-creating-notebooks-hcc.md
    - file: notebooks/05-example-notebook.ipynb
site:
  template: book-theme
```

You can also auto-generate the `toc` list from whatever files already
exist in the folder:

```bash
jupyter-book init --write-toc
```

## Adding content

Every chapter is either:
- a **Markdown file** (`.md`) — plain narrative content, like this page, or
- a **Jupyter Notebook** (`.ipynb`) — for worked examples where you want
  live, executed code and output as part of the page (see
  [Chapter 5](notebooks/05-example-notebook.ipynb)).

Add the new file to the `toc` list in `myst.yml` in the order you want it
to appear.

## Executing notebooks as part of the build

If a notebook chapter's outputs aren't already saved (or you want to
guarantee they're current), add `--execute` to build or preview commands
so MyST runs every notebook fresh before rendering it into the site —
the same "restart and run all" discipline covered in
[Chapter 3](03-notebook-anatomy.md), applied automatically at build time.

## Previewing locally

```bash
jupyter-book start
```

This serves a live-reloading local copy of the site — edit a file, save,
and the browser preview updates.

## Building a static site to publish

```bash
jupyter-book build --html
```

This produces a static site (HTML, CSS, JS, and any notebook outputs)
that you can host anywhere that serves static files — GitHub Pages, a
university web server, or Canvas as linked content.

## Publishing to GitHub Pages

1. Push the project folder (source files, **not** the build output) to a
   GitHub repository.
2. Build the static site: `jupyter-book build --html`.
3. Push the contents of the build output to a `gh-pages` branch, or
   configure a GitHub Actions workflow to do this automatically on every
   push to `main`. The [MyST documentation](https://mystmd.org/guide/deployment)
   has a ready-to-use GitHub Actions template for this.
4. In the repository's **Settings → Pages**, point GitHub Pages at the
   `gh-pages` branch.

## Keeping this book updated

To extend this training module for a future semester:

1. Add or edit `.md` / `.ipynb` files in this project folder.
2. Add any new file to the `toc` in `myst.yml`.
3. Run `jupyter-book start` to preview.
4. Rebuild and republish as above.

Next: [Quick Reference & Troubleshooting](08-quick-reference.md)
