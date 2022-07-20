# Contextual Dynamics Lab LaTeX template for grant proposals and full-page documents

This template repository (forked from our [primary LaTeX template repository](https://github.com/ContextLab/latex-base)) provides a convenient way of setting up new grant applications and other LaTeX documents that use full-page formatting or space constraints.  The template includes our lab-recommended systems for organizing LaTeX code (including bibliography and figures). The repository also includes scripts for automatically setting up the repository and compiling the latex files into PDFs.

# Using this template repository

There are two simple ways of using this repository as a template for a new project:

1. Visit the [GitHub page](https://github.com/ContextLab/latex-base) for this project and click the green "Use this template" button.  You will be taken to a new page that enables you to name and configure your new repository.
2. Create a [new GitHub repository](https://github.com/new) and select "ContextLab/latex-template" from the "Repository template" dropdown menu.  Then name and configure your repository from the same page.

# Basic setup

After cloning your new repository, run the `setup.sh` script** in Terminal:
```bash
sh setup.sh
```
This will initialize the CDL-bibliography repository as a sub-module of your project for convenient bibliography management.

# Recommended organization

If you are writing a grant application or another document that requires additional documentation or files, the lab-recommended approach to organizing files is the following:
```
root
└── all files needed to generate a PDF of your document(s)
└── figs : pdf copies of each figure
    └── source: source files used to construct individual figure panels or components
├── CDL-bibliography: bibliography management based on https://github.com/ContextLab/CDL-bibliography
└── admin: files and documents related to administrative tasks (e.g., cover letters, forms, budget spreadsheets, etc.)  
```