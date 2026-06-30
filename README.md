# PFE Report LaTeX Template

A ready-to-use LaTeX template for an end-of-studies (PFE) report. Edit the chapters, compile, and you have a report. [Chapter 1](chapters/chapter1.tex) shows how to add figures, tables, code, and citations.

A few things to look at first:

- [Example report](examples/report/Graduation%20Project%20Report.pdf): a finished report built from this template, so you know what the result looks like.
- [Example presentations](examples/presentation/): my defense slides and a few other PFE presentations from the company. Take inspiration from them.
- [INSAT Report Notes.pdf](INSAT%20Report%20Notes.pdf): INSAT's notes on what a PFE report should contain.

## Compile it

**Overleaf (no install).** Zip this folder, create a New Project in Overleaf, choose Upload Project, and open [main.tex](main.tex). Set the compiler to pdfLaTeX in the menu. It builds the bibliography for you.

**VS Code + MiKTeX (local).**

1. Install [MiKTeX](https://miktex.org/download) and the LaTeX Workshop extension.
2. Open this folder in VS Code, then open [main.tex](main.tex).
3. Save the file to build it (or run *LaTeX Workshop: Build LaTeX project*). The PDF comes out as `main.pdf` in the project root, and the `.aux` and `.log` files it leaves behind are git-ignored.

If you want to keep the root clean, add a `.vscode/settings.json` (it is git-ignored, so make your own) with this line, which sends the build output to a separate `build/` folder instead:

```json
"latex-workshop.latex.outDir": "%DIR%/build"
```

## Edit the cover and last page

These two pages are PDFs that [main.tex](main.tex) includes, so you edit them outside LaTeX. Keep the same file names when you save.

| Page | Source | How to edit |
|------|--------|-------------|
| Cover | [PageDeGarde_English.docx](PageDeGarde_English.docx) | Edit in Word and export to PDF, keeping the name `PageDeGarde_English.pdf`. |
| Last page | [LastPage.docx](LastPage.docx) | Edit in Word and export to PDF, keeping the name `LastPage.pdf`. |

If you want something more designed, open the `.pdf` in Canva, edit it, download it as a PDF, and replace the original (keep the name).

## Write your report

Your chapters live in [chapters/](chapters/), together with the general introduction and conclusion. The front and back matter (abstract, résumé, acknowledgements, and so on) sits in [preliminary pages/](preliminary%20pages/). To add or remove a chapter, edit the `\input` lines in [main.tex](main.tex). Images go in [assets/](assets/), and references go in [preliminary pages/bibliography.bib](preliminary%20pages/bibliography.bib).
