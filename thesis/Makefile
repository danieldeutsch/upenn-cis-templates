.SUFFIXES: .tex .in .dvi .ps .pdf
all: thesis.pdf 
.tex.pdf: 
	pdflatex $<
	-bibtex $*
	pdflatex $<
	pdflatex $<
introduction.pdf:
	pdflatex introduction.tex
	bibtex introduction.aux
	pdflatex introduction.tex
	pdflatex introduction.tex
chapter1.pdf: chapter1
	pdflatex chapter1/chapter1.tex
	bibtex chapter1.aux
	pdflatex chapter1/chapter1.tex
	pdflatex chapter1/chapter1.tex
chapter2.pdf: chapter2
	pdflatex chapter2/chapter2.tex
	bibtex chapter2.aux
	pdflatex chapter2/chapter2.tex
	pdflatex chapter2/chapter2.tex
conclusion.pdf:
	pdflatex conclusion.tex
	bibtex conclusion.aux
	pdflatex conclusion.tex
	pdflatex conclusion.tex
clean:
	rm -f *.aux *.dvi *.ps *.bbl *.blg *.out *.log *.toc *.lof *.lot *.nav *.snm *.bak *~ *.acn *.ist *.syg *.acn *.glsdefs *.ist *.syg thesis.pdf introduction.pdf chapter1.pdf chapter2.pdf conclusion.pdf
