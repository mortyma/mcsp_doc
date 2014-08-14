PROJECT = protocol

.PHONY: all clean

all: $(PROJECT).pdf

$(PROJECT).tex: $(PROJECT).Rnw functions.Rnw sources.bib
	R CMD Sweave $(PROJECT).Rnw

$(PROJECT).pdf: $(PROJECT).tex $(PROJECT).Rnw 
	R CMD latexmk -pdf $(PROJECT).tex

clean:
	latexmk -CA
	rm -f protocol.tex
	rm -f *.pdf
	rm -f *.backup
