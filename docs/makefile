TEX_SRCS := $(wildcard *.tex)
PDFS := $(TEX_SRCS:%.tex=%.pdf)
PNGS := $(TEX_SRCS:%.tex=%.png)

all: $(PNGS)

%.pdf: %.tex
	pdflatex --file-line-error-style $<

%.png: %.pdf
	convert -density 300 -strip $< -quality 9 $@
