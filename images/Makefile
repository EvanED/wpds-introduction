DOT_FILES=$(wildcard *.dot)
PDF_FILES=$(DOT_FILES:dot=pdf)

all: $(PDF_FILES) cegar.pdf

%.pdf: %.dot
	dot -Tpdf -o$@ $^

%.pdf: %.svg
	inkscape --export-pdf=$@ --export-area-drawing --without-gui $^
