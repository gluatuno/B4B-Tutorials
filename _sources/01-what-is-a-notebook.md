# What Is a Jupyter Notebook?

A **Jupyter Notebook** is a single document (a `.ipynb` file) that mixes
three things together, in order, top to bottom:

- **Code** you can run, one small piece at a time
- **Output** — whatever that code produces: numbers, tables, plots, error
  messages
- **Narrative text** (written in Markdown) explaining what you did and why

Because code, results, and explanation live in the same file, a notebook
can serve as both your *lab notebook* and your *analysis pipeline* at
once. That is exactly why it is required alongside your written reports
for the course project: it is the one artifact where an instructor can
see your commands, your output, and your reasoning together, without
having to reproduce anything by hand.

## Why not just paste code into a Word document?

A few reasons this course uses live notebooks instead:

| | Pasted code in a report | Jupyter Notebook |
|---|---|---|
| Can the grader re-run it? | No | Yes |
| Does it show real output? | Only if you paste it in (and it may go stale) | Yes, output is attached to the code that made it |
| Can you fix one step without retyping everything? | No | Yes |
| Does it catch your own mistakes? | Not until you compile a report | Immediately — cells that error are visible |

## What a notebook is *not*

- It is not a place to dump raw command history with no explanation —
  see [Chapter 4](04-writing-good-notebooks.md) for what "well
  documented" means here.
- It is not a substitute for your written proposal, progress report, or
  final paper — it is a companion to them.
- It is not tied to any one dataset or tool. You will use the same
  notebook skills whether you are running BLAST, aligning sequences,
  parsing a GenBank file, or building a phylogenetic tree.

```{admonition} Where this fits in the course
:class: note
The Course Project Guideline requires a Jupyter Notebook alongside your
Progress Report and Final Paper. This training module teaches the
mechanics; the Guideline document tells you exactly what is graded.
```

Next: [Creating a Notebook on HCC / Open OnDemand](02-creating-notebooks-hcc.md)
