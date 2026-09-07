# Notebook Anatomy: Cells and Kernels

A notebook is built out of **cells**. Understanding the two cell types —
and the one running process behind them — is really all the mechanics
you need.

## Cell types

**Code cells** contain Python (or another language) that runs when you
execute the cell. Any output — printed text, a table, a plot, an error —
appears directly beneath it.

**Markdown cells** contain formatted text: headers, bullet points, bold
text, links, even equations. This is where you explain your reasoning.
Double-click a Markdown cell to edit it; run it (`Shift+Enter`) to render
it.

```{admonition} Try it
:class: tip
Click a cell, press `Esc` then `M` to turn it into a Markdown cell, or
`Esc` then `Y` to turn it into a code cell. Press `Enter` to go back to
editing.
```

## Running cells

- `Shift+Enter` — run the current cell, move to the next
- `Ctrl+Enter` — run the current cell, stay on it
- `Alt+Enter` — run the current cell, insert a new one after it

## The kernel: one running process per notebook

The **kernel** is the live Python process behind your notebook. It holds
all your variables, imports, and loaded data in memory. This has two
practical consequences:

1. **Run order matters, not just cell order on the page.** If you run
   cell 5, then go back and edit cell 2, cell 5 does *not* automatically
   re-run. The notebook can end up in a state that doesn't match what's
   on screen. This is the single most common way student notebooks break.
2. **You can (and should) restart it.** Use **Kernel → Restart Kernel and
   Run All Cells** before you consider a notebook "done." If it runs
   cleanly top-to-bottom on a fresh kernel, you know it's actually
   reproducible — not just held together by leftover variables from
   cells you ran out of order twenty minutes ago.

```{admonition} Before every submission
:class: warning
Run **Kernel → Restart Kernel and Run All Cells**. If this doesn't
complete cleanly, your grader's copy won't either.
```

## The execution count

The number in brackets next to a code cell (e.g., `[7]`) tells you *when*
that cell was last run relative to the others — not its position on the
page. Out-of-order numbers (like `[3]` appearing after `[9]`) are a red
flag that the notebook wasn't run top-to-bottom before saving.

Next: [Writing a Notebook That Grades Well](04-writing-good-notebooks.md)
