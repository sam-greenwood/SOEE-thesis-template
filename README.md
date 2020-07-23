# SOEE-thesis-template
Latex thesis template for the School of Earth and Environment, University of Leeds.


This template is based upon a series of iterative updates from pervious students. The previous version, which was formatted for the alternative thesis, can be found at https://github.com/matthew-gaddes/alternative_format_thesis

I have modified this for the standard thesis format, added in the nomenclature list using the nomencl package and tested the template for Overleaf. Formatting for the standard thesis simply required removing the refsection environment from each chapter, which can easily be reintroduced.

```latex
\begin{refsection}


\end{refsection}
\printbibliography[heading=subbibliography]
```

To compile the document, either simply use your preffered application, Overleaf, or you can use the included Makefile to compile from the command line. Running `make` will use pdflatex to create the pdf and biber to produce the references. Assuming you are using the nomencl package (see template) for the nomenclature list, then the Makefile uses makeindex to include this.  in to the Makefile to get it to . You can also run `make clean` to move all the auxiliary files into a folder to keep things neat. I'll admit I was a little lazy and hardcoded in the auxiliary files extensions, so you may get an warning if it tries to move files with an extension that doesn't currently exist but this won't cause it to fail. `make` automatically calls `make clean` when it finishes.
