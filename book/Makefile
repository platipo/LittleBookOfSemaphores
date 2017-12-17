NAME = LittleBookOfSemaphores

.PHONY: book all clean

all: book

book: book.tex
	latexmk -jobname="$(NAME)" -pdf -pdflatex="pdflatex -interaction=nonstopmode" -use-make $< 

clean:
	latexmk -jobname="$(NAME)" -c
