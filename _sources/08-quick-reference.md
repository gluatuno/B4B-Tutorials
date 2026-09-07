# Quick Reference & Troubleshooting

## Keyboard shortcuts

| Action | Shortcut |
|---|---|
| Run cell, move to next | `Shift + Enter` |
| Run cell, stay on it | `Ctrl + Enter` |
| Run cell, insert new one after | `Alt + Enter` |
| Convert cell to Markdown | `Esc` then `M` |
| Convert cell to code | `Esc` then `Y` |
| Insert cell above / below | `Esc` then `A` / `B` |
| Delete cell | `Esc` then `D`, `D` |

## Pre-submission checklist

- [ ] **Kernel → Restart Kernel and Run All Cells** completes with no
      errors
- [ ] Execution counts (`[1]`, `[2]`, …) are in order top to bottom
- [ ] Section headers match your written report
- [ ] Every figure/table is labeled and referenced in the surrounding text
- [ ] No hard-coded personal file paths
- [ ] Package/tool versions are noted near the top
- [ ] File renamed to `lastname_deliverable.ipynb`
- [ ] Exported to HTML or PDF, named to match
- [ ] Both files (`.ipynb` and exported copy) included in your submission

## Common problems

**"My notebook worked a minute ago and now it's throwing errors."**
Something upstream changed or was run out of order. Restart the kernel
and run all cells from the top — see [Chapter 3](03-notebook-anatomy.md).

**"A cell is stuck with `[*]` and never finishes."**
The kernel is busy or hung. Use **Kernel → Interrupt Kernel**; if that
doesn't work, **Kernel → Restart Kernel**.

**"PDF export fails."**
PDF export depends on a LaTeX installation that isn't always available.
Export to HTML instead — it's the recommended default in this course
(see [Chapter 6](06-exporting-notebooks.md)).

**"My file paths worked on my laptop but not on HCC."** Paths are almost
never portable between machines. Use paths relative to your notebook's
own folder, or fetch data programmatically inside the notebook.

**"I lost my HCC session / it timed out."**
Your files are saved on disk and persist between sessions. Just launch a
new JupyterLab session from Open OnDemand
(see [Chapter 2](02-creating-notebooks-hcc.md)) and reopen your notebook.

## Where to get help

- Office hours: 514D Allwine Hall
- HCC Open OnDemand: swan-ood.unl.edu (allocation group `glu4class`)
