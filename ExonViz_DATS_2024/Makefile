FNAMES:= CYLD.png DMD-schematic.png SDHD.png SDHD-non.png
FIGURES:= $(addprefix images/, $(FNAMES))

ALL: poster_portrait.pdf

%.pdf: %.tex Makefile $(FIGURES)
	pdflatex --enable-write18 $< &&	pdflatex $< && pdflatex $<

%.png: %.svg
	inkscape --export-dpi=300 --export-filename $@ $<
clean:
	  rm -f *.aux	*.bbl	*.blg	*.log	poster.pdf 
