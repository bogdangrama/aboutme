TEX_EN = Alexandru_Burghelea_CV_en.tex
PDF_EN = $(TEX_EN:.tex=.pdf)
PDFLATEX = pdflatex
CLEAN_FILES = *.aux *.log *.out *.synctex.gz

.PHONY: clean all

all: $(PDF_EN)

$(PDF_EN): %.pdf: %.tex
	$(PDFLATEX) $<
	$(PDFLATEX) $<	# Twice, so TOC is also updated
clean-all:
	-rm -f $(CLEAN_FILES) *~ $(PDF_EN)

clean:
	-rm -f $(CLEAN_FILES) *~ 
