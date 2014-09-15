# PRESENTLY DEFUNCT

# University of Rochester Dissertation Template

This repository contains a LaTeX template for dissertations at the University
of Rochester.  It is, to my knowledge, consistent with
[UR regulations](http://www.rochester.edu/theses/ThesesManual.pdf) as of
July 2014.  Use at your own risk.  If the requirements change or you notice an
inconsistency, please submit an issue or pull request and I'll try to update
the template.

Example output is available [here](dissertation.pdf?raw=true).


## Files

The template consists of the following files:

  * `dissertation.tex`: The master document, which includes all packages and
    all content files.

  * `title.tex`: Title page, formatted per guidelines

  * `dedication.tex`: Dedication (optional)

  * `bio.tex`: Biographical Sketch, including sample text

  * `acknowledgments.tex`: Acknowledgments (optional)

  * `abstract.tex`: Abstract

  * `contrib.tex`: Contributors and Funding Sources, including sample text

  * `contents.tex`: Table of Contents, List of Tables, and List of Figures

  * `chapter-first.tex` and `chapter-second.tex`: Sample chapters

  * `references.tex`: References/bibliography (bib file `sample.bib`)


## Building and Cleaning

I recommend using
[Latexmk](http://users.phys.psu.edu/~collins/software/latexmk-jcc/) to build
the output.  Latexmk runs LaTeX and BibTeX successively until the final
product is complete, so you don't have to worry about the dreaded **??**
showing up where a reference should be.

```bash
# Compile the dissertation
latexmk -pdf dissertation

# Remove auxiliary files, log files, etc., after compilation
latexmk -c

# Remove all generated files, including PDFs
latexmk -C
```
