# Writing a Notebook That Grades Well

This chapter expands on the six criteria in the
**Jupyter Notebook Requirements** section of the Course Project
Guideline: platform, structure, reproducibility, documentation, output,
and submission. Each one below includes what it looks like done well and
what it looks like done poorly.

## Structure: mirror your paper's sections

Use Markdown headers that match your written report, so a grader can move
between the two without getting lost.

```markdown
# Project Title

## Data & Methods
...

## Results
...
```

A notebook with no headers, or headers that don't correspond to anything
in your paper, forces the grader to reverse-engineer your logic. A
notebook with clear section headers lets them check your work against
your paper section by section.

## Reproducibility: it has to actually run

- Run **Kernel → Restart Kernel and Run All Cells** before submitting
  (see [Chapter 3](03-notebook-anatomy.md)).
- Note tool and package versions somewhere near the top, e.g.:

```python
import Bio
print(Bio.__version__)
```

- Avoid paths that only exist on your account, like
  `/home/jsmith123/my_stuff/data.fasta`. If a file is small, keep it in
  the same project folder and use a relative path (`data/sequence.fasta`).
  If it's a public dataset, download it inside the notebook (e.g. via
  `Bio.Entrez` or a direct URL) so the retrieval step is itself part of
  the reproducible record.

**Weak:** a notebook that only runs because of a variable you set by hand
in the Python console last week and never wrote into a cell.

**Strong:** a notebook a classmate could open, run top to bottom, and get
your figures.

## Documentation: explain the *why*, not just the *what*

The code already shows *what* you did. Markdown cells are for *why* you
did it and *what it means*.

**Weak** (code-only, no narration):

```python
result = pairwise2.align.globalxx(seq1, seq2)
print(result[0])
```

**Strong** (same code, framed):

```markdown
### Pairwise alignment of the candidate ORF against the reference

We align the two sequences globally, since we expect similarity across
their full length rather than in a short local region.
```

```python
from Bio.Align import PairwiseAligner
aligner = PairwiseAligner()
aligner.mode = "global"
alignment = aligner.align(seq1, seq2)[0]
print(alignment)
```

```markdown
The alignment shows ~94% identity, consistent with the candidate ORF
being a close homolog rather than a novel gene family.
```

That last line — the interpretation — is often the single biggest
difference between a notebook that reads as "I ran some commands" and one
that reads as "I did an analysis."

## Output: generate it here, don't paste it in

Figures and tables should be produced by code in the notebook, not copied
in from somewhere else (a screenshot, a different script, a spreadsheet
you edited by hand). Label every figure and table and refer to it by
number in your surrounding text, the same way you would in the paper
itself.

## Platform: use the course environment

Develop and run on JupyterLab via HCC Open OnDemand
(`swan-ood.unl.edu`, group `glu4class`) — see
[Chapter 2](02-creating-notebooks-hcc.md). This keeps everyone on the
same package versions and avoids "works on my machine" problems.

## Submission: two files, not one

Submit **both**:
1. The live `.ipynb` file
2. An exported PDF or HTML copy

See [Chapter 6](06-exporting-notebooks.md) for how to export. The static
copy is what a grader opens first; the live file is what they open if
they need to check something by re-running it.

```{admonition} Undergraduate vs. graduate expectations
:class: note
The mechanics in this chapter are the same for everyone. What differs by
level is depth: graduate notebooks are expected to include more thorough
interpretation, and where applicable, a brief discussion of algorithmic
or parameter choices — not just more cells.
```

Next: [Worked Example: A Small Bioinformatics Notebook](notebooks/05-example-notebook.ipynb)
