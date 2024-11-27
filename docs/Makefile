# LaTeX Compiler
LC = pdflatex
LCFLAGS = -quiet

TITLE = Pygmy Flight Computer Manual
OUT = $(TITLE).pdf

MAIN = main.tex

all: $(OUT)

rebuild: clean all

$(OUT):
	@$(LC) $(LCFLAGS) -jobname="$(TITLE)" $(MAIN)

clean:
	@rm "$(TITLE)".*
	@rm indent.log
