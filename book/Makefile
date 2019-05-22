SRC := book.tex
NAME := LittleBookOfSemaphores
COMPACT := LittleBookOfSemaphoresCompact

.PHONY: book compact all clean

all: book compact

book: $(SRC)
	latexmk -jobname="$(NAME)" -pdf -silent -pdflatex="pdflatex -interaction=nonstopmode" -use-make $< 

compact: $(SRC)
	$(eval TFILE:=$(shell mktemp -p . --suffix=.tex))
	sed -e 's/%\\notcompactfalse/\\notcompactfalse/' -e 's/\\notcompacttrue/%\\notcompacttrue/' $< > $(TFILE)
	latexmk -jobname="$(COMPACT)" -pdf -silent -pdflatex="pdflatex -interaction=nonstopmode" -use-make $(TFILE)
	@rm $(TFILE)

clean:
	latexmk -jobname="$(NAME)" -c $(SRC)
	latexmk -jobname="$(COMPACT)" -c $(SRC)
