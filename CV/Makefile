TEX_EN = Alexandru_Burghelea_CV_en.tex
TEX_RO = Alexandru_Burghelea_CV_ro.tex
PDF_EN = $(TEX_EN:.tex=.pdf)
PDF_RO = $(TEX_RO:.tex=.pdf)
PDFLATEX = pdflatex
CLEAN_FILES = *.aux *.log *.out *.synctex.gz

.PHONY: clean all

all: $(PDF_EN) $(PDF_RO)

$(PDF_EN) $(PDF_RO): %.pdf: %.tex
	$(PDFLATEX) $<
	$(PDFLATEX) $<	# Twice, so TOC is also updated
clean-all:
	-rm -f $(CLEAN_FILES) *~ $(PDF_EN) $(PDF_RO) 

clean:
	-rm -f $(CLEAN_FILES) *~ 
