# Contextual Dynamics Lab LaTeX template for grant proposals and full-page documents

This template repository (forked from our [primary LaTeX template repository](https://github.com/ContextLab/latex-base)) provides a convenient way of setting up new grant applications and other LaTeX documents that use full-page formatting or space constraints.  The template includes our lab-recommended systems for organizing LaTeX code (including bibliography and figures).

# Using this template repository

1. **Set up the shared lab bibliography.**  You only need to do this once per computer.  Install `cdlbib` by following the [CDL-bibliography installation instructions](https://github.com/ContextLab/CDL-bibliography#installation), and then run
```bash
cdlbib setup
```
This makes the lab's shared bibliography (`cdl.bib`) available to every LaTeX document on your computer.  The template's `main.tex` file is already set up to use it (`\bibliography{cdl}`).  See the [CDL-bibliography documentation](https://github.com/ContextLab/CDL-bibliography) for instructions on adding new references.

2. **Create a new repository from this template.**  Visit the [GitHub page](https://github.com/ContextLab/latex-base-grants) for this project and click the green "Use this template" button, or create a [new GitHub repository](https://github.com/new) and select "ContextLab/latex-base-grants" from the "Repository template" dropdown menu.  Then name and configure your repository.  The official version of each project lives under the [ContextLab](https://github.com/ContextLab) organization.

3. **Fork the new repository, and do your work in your fork.**  Work from individual lab members should always happen in a fork (`<username>/<repository name>`) of the ContextLab repository.  To update the ContextLab (upstream) repository, submit a pull request from your fork.

To compile your document, run `pdflatex`, then `bibtex`, and then `pdflatex` twice more:
```bash
pdflatex main
bibtex main
pdflatex main
pdflatex main
```

## Using Overleaf

You can also draft your document on [Overleaf](https://www.overleaf.com/).  If you do, be sure to [sync your Overleaf project with a GitHub repository](https://docs.overleaf.com/integrations-and-add-ons/git-integration-and-github-synchronization/github-synchronization) as well.  Overleaf projects can't use the bibliography installed on your computer; follow [these instructions](https://github.com/ContextLab/CDL-bibliography#using-the-bibtex-file-on-overleaf) to link the shared bibliography into your Overleaf project instead.

# Recommended organization

If you are writing a grant application or another document that requires additional documentation or files, the lab-recommended approach to organizing files is the following:
```
root
└── all files needed to generate a PDF of your document(s)
└── figs : pdf copies of each figure
    └── source: source files used to construct individual figure panels or components
└── admin: files and documents related to administrative tasks (e.g., cover letters, forms, budget spreadsheets, etc.)  
```
