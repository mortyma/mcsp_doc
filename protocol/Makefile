PROJECT = protocol

.PHONY: all clean

all: $(PROJECT).pdf

$(PROJECT).tex: $(PROJECT).Rnw
	R CMD Sweave $(PROJECT).Rnw

$(PROJECT).pdf: $(PROJECT).tex
	latexmk -pdf -use-make $(PROJECT).tex

clean:
	latexmk -CA
