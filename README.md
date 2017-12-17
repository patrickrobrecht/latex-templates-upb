# LaTeX Thesis Template @UPB

This LaTeX template may be used by students of Computer Science
and other scientific studies at the
[University of Paderborn](https://cs.uni-paderborn.de/) (UPB)
as basic setup for their Bachelor's / Master's / PhD thesis.
The same template may be used for thesis proposals as well.

## How to use

### Thesis template
- Open the file `thesis/thesis.tex` in your favourite LaTeX editor
    (e. g. [TeXstudio](http://texstudio.sourceforge.net/)
    and compile it with PdfLaTeX and BibTeX:
    ```
    cd thesis
    pdflatex thesis
    bibtex thesis
    pdflatex thesis
    pdflatex thesis
    ```
- Set your title, thesis type, name etc. in `config.tex`.
    These will be used on the title page, the PDF title, and the footers.
- Start writing your thesis:
  - Write the abstract `thesis/pretext/abstract.tex`
  - Write your introduction in `thesis/chapters/introduction.tex`.
  - Add more chapters by adding `\input{chapters/my-fancy-second-chapter}`
        to the main part of `thesis/thesis.tex`
        and put the contents for the second chapter 
        into the created file `chapters/my-fancy-second-chapter.tex`.

Helpful resources:
- [WikiBooks: LaTeX](https://en.wikibooks.org/wiki/LaTeX)
- [Getting Started with LaTeX](https://www.maths.tcd.ie/~dwilkins/LaTeXPrimer/GSWLaTeX.pdf)

### Bibliography management
- The bibliography file `literature.bib` can be managed
    using [JabRef](http://www.jabref.org/) or any other tool for bibtex.
    After adding/editing an entry in the bibliography you may need 
    to recompile LaTeX twice until the reference is shown/updated.

Helpful resources:
- [How to use BibTeX](http://www.bibtex.org/Using/)
- [ShareLaTeX: Bibliography management in LaTeX](https://www.sharelatex.com/learn/Bibliography_management_in_LaTeX)
- [WikiBooks: LaTeX/Bibliography Management](https://en.wikibooks.org/wiki/LaTeX/Bibliography_Management)

### Slides template
- Open the file `slides/slides.tex` in your favourite LaTeX editor
    and compile it with PdfLaTeX:
    ```
    cd slides
    pdflatex slides
    ```
- Start designing your slides:
    - Write your introduction in `slides/sections/introduction.tex`.
    - Add more sections by creating `slides/sections/mysection.tex`.
        and include it in the main file with `\input{chapters/my-section}`.

Helpful resources:
- [The beamer class - User guide](http://mirrors.ctan.org/macros/latex/contrib/beamer/doc/beameruserguide.pdf)
- [ShareLaTeX: Beamer](https://www.sharelatex.com/learn/Beamer)
- [WikiBooks: LaTeX/Presentations](https://en.wikibooks.org/wiki/LaTeX/Presentations)
- [Fun with Beamer](http://web.mit.edu/rsi/www/pdfs/beamer-tutorial.pdf)
    (tutorial by Prathik Naidu and Adam Pahlava)

### Common configuration
- You may add more packages to import
    or define [own commands](https://www.sharelatex.com/learn/Commands#!#Defining_a_new_command)
    in `command.tex`.
    They can be used both in the thesis and the slides.

### Manage todos
Many LaTeX editors recognize the commands
- `%TODO mytodo`
- and `\todo{mytodo}`

and create a list of todos for you.

Note that the latter requires the todonotes package (included in the template)
    which will create boxes in the generated PDF showing your todos,
    while comments like `%TODO mytodo` won't appear in the PDF.

### Not from UPB, but still like the template?
You may replace the file `figures/logo.png` with any other logo.


## How to contribute
You have ideas how to improve this template?
Or found problems?

- [Fork the repository](https://help.github.com/articles/fork-a-repo/)
    and create a [pull request](https://help.github.com/articles/creating-a-pull-request-from-a-fork/).
- Report an [issue](https://github.com/patrickrobrecht/latex-templates-upb/issues).
