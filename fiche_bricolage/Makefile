.PHONY: default
default: all

files=generale.tex tournevis.tex perceuse.tex fer_a_souder.tex colle.tex scie_sauteuse.tex contact.tex

.PHONY: brochure
brochure: brochure_bricolage.pdf
.PHONY: poster
poster: poster_bricolage.pdf

.PHONY: all
all: brochure poster

.PHONY: force
force: clean-all $(output)

%.pdf: %.tex $(files)
	@echo "Compile the LaTeX" > /dev/stderr
	pdflatex $<
	@echo "Compile the LaTeX" > /dev/stderr
	pdflatex $<

#Add dependency to the sty
poster_bricolage.pdf: template_poster.sty

.PHONY: clean
clean:
	rm -f *.aux *.blg *.log *.out *.ps

.PHONY: clean-all
clean-all: clean
	rm -f *.pdf

.PHONY: help
help:
	@echo "Possible targets:"
	@echo "     all (default)"
	@echo "     force"
	@echo "     brochure"
	@echo "     poster"
	@echo "     clean"
	@echo "     clean-all"
