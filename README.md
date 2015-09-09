# sample-thesis

This is a repository containing a skeleton LaTeX document for generating University of Hawaii theses.

It uses  [LaTeX UHM Thesis Style, v 2.2.0beta](https://github.com/rbrewer/latex-uhm-thesis/releases/tag/v2.2.0beta).

To use this, I recommend downloading and installing [TexLive 2015](https://www.tug.org/texlive/).

The sample document is organized in the following way:

uhthesis.cls  (The style file.)

thesis.tex    (The 'master' file.   Sets up the document, and includes the following files:)

* abstract.tex
* acknowledgements.tex
* dedication.tex
* introduction.tex
* related-work.tex
* design.tex
* results.tex
* conclusion.tex
* references.bib

This repo also includes a convenient Makefile for generating the PDF.  After downloading this repo and installing TexLive, you should be able to generate a PDF version of the sample document (called thesis.pdf) by typing 'make':

```
[~/github/csdl/sample-thesis]-> make
make: *** No rule to make target `body.tex', needed by `thesis.d'.  Stop.
[~/github/csdl/sample-thesis]-> rm -rf thesis.d
[~/github/csdl/sample-thesis]-> make
NOTE: You may ignore warnings about the following files:

     thesis.d

Makefile:2873: thesis.d: No such file or directory
= thesis.tex --> thesis.d thesis.pdf.1st.make (0-1) =
make: *** No rule to make target `body.tex', needed by `thesis.d'.  Stop.
[~/github/csdl/sample-thesis]-> make
NOTE: You may ignore warnings about the following files:

     thesis.d

Makefile:2873: thesis.d: No such file or directory
= thesis.tex --> thesis.d thesis.pdf.1st.make (0-1) =
= example.bib thesis.aux --> thesis.bbl =
= thesis.tex --> thesis.pdf (1-2) =
= thesis.tex --> thesis.pdf (1-3) =
Overfull \hbox (161.81332pt too wide) in paragraph at lines 19--22
[]\OT1/cmr/m/n/10.95 Here is an URL which can-not be bro-ken, lead-ing to ter-r
i-ble out-put $\OML/cmm/m/it/10.95 <$\OT1/cmr/m/n/10.95 http://www.hotwired.com
/webmonkey/98/16/index2a.html$\OML/cmm/m/it/10.95 >$ 
 []

Success!  Wrote 16 pages, 138631 bytes to thesis.pdf
```

The gitignore file is set up to exclude all the intermediate files from being committed to the repo.  You can also do 'make clean' to get rid of them (but this will also delete the PDF file.)
