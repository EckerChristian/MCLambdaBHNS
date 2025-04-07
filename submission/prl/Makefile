#TEX    = xelatex
TEX    = pdflatex
# TEX    = platex
LDIFF  = latexdiff
BIBTEX = bibtex
EBB    = ebb
DVIPDF = dvipdfm
DVIPS  = dvips
PS2PDF = ps2pdf
RM     = /bin/rm -rf
OPT    = # -shell-escape   ### for PNG

TEXT   = paper
DIFF   = diff


ps:
#
#	$(EBB)     ./FIG/*.pdf
#	
	$(TEX)     $(OPT) $(TEXT).tex
	$(BIBTEX)  $(TEXT)
	$(TEX)     $(OPT) $(TEXT).tex
#	$(TEX)     $(OPT) $(TEXT).tex
#
#	$(DVIPDF)  $(TEXT).dvi
#	$(DVIPS)   -t a4 $(TEXT).dvi -o
#	$(PS2PDF)  $(TEXT).ps

diff:
#
#	
	$(LDIFF)   $(OLD).tex $(TEXT).tex > $(DIFF).tex
	$(TEX)     diff.tex
	$(BIBTEX)  $(DIFF)
	$(TEX)     diff.tex


clean:
	$(RM)  *.dvi  *.log  *.aux  *.blg  *.bbl  *.out  *Notes.bib  *~


clean_all:
	$(RM)  *.dvi  *.log  *.aux  *.pdf  *.ps 
	$(RM)  ./figs/*.bb
