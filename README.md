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

  * `01-title.tex`: Title page, formatted per guidelines

  * `02-dedication.tex`: Dedication (optional)

  * `03-bio.tex`: Biographical Sketch, including sample text

  * `04-acknowledgments.tex`: Acknowledgments (optional)

  * `05-abstract.tex`: Abstract

  * `06-contrib.tex`: Contributors and Funding Sources, including sample text

  * `07-contents.tex`: Table of Contents, List of Tables, and List of Figures

  * `08-chapter-01.tex` and `08-chapter-02.tex`: Sample chapters

  * `09-references.tex`: References/bibliography (bib file `sample.bib`)

The inclusion of the numerals preceding the descriptive names leads to an order
of the files based on file names that is consistent with their logical order.

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

In addition, the file `makefile` is set up to do the same as the `latexmk`
commands above. To use it, instead run the following:

```bash
# Compile the dissertation
make

# Remove auxiliary files, log files, etc., after compilation
make clean

# Remove all generated files, including PDFs
make fullclean
```

One advantage of the `makefile` approach is that you can extend the definitions
and use [make](http://en.wikipedia.org/wiki/Make_(software)) to accomplish
*much*, *much* more than just building LaTeX documents.
