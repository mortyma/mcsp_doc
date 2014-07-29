PROJECT = protocol

.PHONY: all clean

all: $(PROJECT).pdf

$(PROJECT).tex: $(PROJECT).Rnw
	R CMD Sweave $(PROJECT).Rnw

$(PROJECT).pdf: $(PROJECT).tex $(PROJECT).Rnw
	R CMD pdflatex $(PROJECT).tex

clean:
	latexmk -CA
	rm protocol.tex
