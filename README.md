# Bioinformatics for Biologists (B4B) - Course Tutorials

Welcome to the central tutorial and resource repository for the **Bioinformatics for Biologists** course at the University of Nebraska at Omaha. 

This repository contains all the foundational guides, coding environment instructions, and project workflows needed to successfully complete your computational biology assignments and final course project.

## 📖 Course Contents

### 1. Environment Setup
Before writing code, you need to configure your workspace. These guides cover access and setup for our high-performance computing resources.
* **Accessing the Holland Computing Center (HCC):** Logging in and navigating the cluster.
* **Open OnDemand:** Launching interactive web-based sessions.
* **Environment Configuration:** Setting up Python, R, and necessary bioinformatics packages.

### 2. Jupyter Notebooks
Jupyter Notebooks are the primary medium for our course assignments and projects.
* **Notebook Basics:** Understanding the anatomy of a notebook (markdown vs. code cells, kernels).
* **Creating & Executing:** Writing clean, reproducible code blocks.
* **Exporting & Submitting:** Saving your notebooks with executed outputs for grading.

### 3. Bioinformatics Workflows
Practical applications of computational tools to biological data.
* **Data Processing:** Handling fasta, fastq, and vcf files.
* **Pipeline Automation:** Stringing together bash commands and Python/R scripts.
* **Data Visualization:** Creating clear, publication-ready graphs from genomic datasets.

### 4. Course Projects
Guidelines for your final bioinformatics project.
* **Structuring Your Analysis:** Best practices for a grading-friendly notebook.
* **Publishing to GitHub:** How to upload your `.ipynb` files to a public repository to build your professional portfolio.

---

## 🛠️ For Instructors & TAs

The overarching training website is built using **Jupyter Book** (v2) and **MyST**. 

If you are a TA or future instructor updating these materials:
1. Edit the source `.md` or `.ipynb` files in the repository.
2. Update the `myst.yml` table of contents if adding new chapters.
3. Rebuild the static site locally using `jupyter-book build --html .`
4. Push the updated `_static` and `.html` files to the `master` branch to automatically update the GitHub Pages site.

For detailed instructions, refer to the [Publishing a Jupyter Book](07-publishing-jupyter-book.html) chapter.

---
*Developed and maintained by Dr. Guoqing Lu | University of Nebraska at Omaha*
