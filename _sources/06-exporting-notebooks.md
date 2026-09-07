# Exporting and Submitting Your Notebook

The Course Project Guideline asks for **two files**: the live `.ipynb`
and an exported PDF or HTML copy. This chapter covers both.

## Before you export

1. **Kernel → Restart Kernel and Run All Cells.** Confirm every cell runs
   without errors and the execution counts are in order
   (see [Chapter 3](03-notebook-anatomy.md)).
2. Check that every figure and table is labeled and that your Markdown
   headers match your paper's section names
   (see [Chapter 4](04-writing-good-notebooks.md)).
3. Save the notebook.

## Exporting from JupyterLab

Use **File → Save and Export Notebook As…**, then choose:

- **HTML** — the simplest, most reliable option; opens in any browser,
  preserves plots and formatting exactly as you saw them. Recommended
  default.
- **PDF** — cleaner for printing, but depends on a working LaTeX
  installation on the server; if it fails or times out, use HTML instead.

If the menu option isn't available in your session, the same export can
be done from a terminal inside JupyterLab (**File → New → Terminal**):

```bash
jupyter nbconvert --to html your_notebook.ipynb
# or
jupyter nbconvert --to pdf your_notebook.ipynb
```

This produces `your_notebook.html` (or `.pdf`) in the same folder.

## What to submit

| Deliverable | Files to include |
|---|---|
| Progress Report | `.ipynb` (live) showing progress so far |
| Final Paper | `.ipynb` **and** exported HTML/PDF |

Name both files consistently with your report, e.g.
`garcia_final_paper.ipynb` and `garcia_final_paper.html`.

```{admonition} Common mistake
:class: warning
Exporting *before* restarting and re-running all cells. The exported
file will faithfully preserve whatever state your notebook was in when
you last saved — including stale output from cells you edited but never
re-ran. Always restart-and-run-all first.
```

Next: [Publishing a Jupyter Book](07-publishing-jupyter-book.md)
