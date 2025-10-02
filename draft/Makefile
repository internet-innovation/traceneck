TEX=pdflatex
BIB=bibtex
TARGET=paper

all: clean pdf

pdf: $(TARGET).pdf

$(TARGET).pdf: $(TARGET).tex $(TARGET).bbl
	$(TEX) $(TARGET).tex
	$(TEX) $(TARGET).tex

$(TARGET).bbl: $(TARGET).aux refs.bib
	$(BIB) $(TARGET)

$(TARGET).aux: $(TARGET).tex
	$(TEX) $(TARGET).tex

clean:
	rm -f *.aux *.bbl *.blg *.log *.out *.toc *.lof *.lot

distclean: clean
	rm -f $(TARGET).pdf