# Creating a Notebook on HCC / Open OnDemand

Everything for this course runs through the Holland Computing Center
(HCC), so there is nothing to install on your laptop. This chapter walks
through launching JupyterLab and creating your first notebook.

## Step 1 — Log in to Open OnDemand

1. Go to **swan-ood.unl.edu** in a browser.
2. Sign in with your university credentials.
3. From the top menu, choose **Interactive Apps → JupyterLab**.

## Step 2 — Request a session

You'll see a form asking for session settings. Use:

- **Account / Allocation:** `glu4class`
- **Partition:** the default/standard partition is fine for coursework
- **Number of hours:** request enough for a working session (2–4 hours is
  typical); you can always start another session later
- **Cores / memory:** the default is sufficient for the analyses in this
  course unless a lab specifically tells you otherwise

Click **Launch**. Your session will queue briefly and then show a
**Connect to JupyterLab** button once it's running.

## Step 3 — Create a new notebook

Once JupyterLab opens:

1. In the **File Browser** on the left, navigate to (or create) a folder
   for this project, e.g. `course_project/`.
2. Click the **+** (Launcher) button, or use **File → New → Notebook**.
3. Choose the **Python 3** kernel (unless a lab specifies otherwise).
4. Immediately rename it something descriptive — click the filename at
   the top of the tab and replace `Untitled.ipynb` with something like
   `lastname_project_progress.ipynb`.

```{admonition} Naming matters
:class: tip
A grader will open dozens of notebooks. `Untitled.ipynb` or
`Untitled17.ipynb` makes their job harder and reflects poorly on your
attention to detail. Use `lastname_deliverable.ipynb`, e.g.
`garcia_final_paper.ipynb`.
```

## Step 4 — Save regularly, and know where your files live

- JupyterLab autosaves periodically, but get in the habit of `Ctrl+S` /
  `Cmd+S` after meaningful progress.
- Files you create live in your HCC home or project directory — they
  persist between sessions. You do **not** need to re-upload anything
  each time you log back in.
- If you need to bring in a dataset, use the file-upload button in the
  File Browser, or download it directly inside a notebook cell (e.g.,
  with `!wget` or `Bio.Entrez`) so the download step itself is part of
  your reproducible record.

Next: [Notebook Anatomy: Cells and Kernels](03-notebook-anatomy.md)
