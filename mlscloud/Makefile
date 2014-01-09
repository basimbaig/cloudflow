all: clean
	latex cloudflow.tex
	bibtex cloudflow
	latex cloudflow.tex
	latex cloudflow.tex
	latex cloudflow.tex
	dvips -t letter -Pcmz cloudflow.dvi -o cloudflow.ps
	ps2pdf cloudflow.ps & 

ps: clean
	latex cloudflow.tex
	bibtex cloudflow
	latex cloudflow.tex
	latex cloudflow.tex
	latex cloudflow.tex
	dvips -t letter -Pcmz cloudflow.dvi -o cloudflow.ps

clean:
	rm -rf *~ *.dvi *.blg *.log .*~ *.aux *.ps *.pdf *.bbl

pdf: 
	ps2pdf -dPDFSETTINGS=/prepress -dSubsetFonts=true -dEmbedAllFonts=true -dMaxSubsetPct=100 -dCompatibilityLevel=1.3 cloudflow.ps 

view:
	ggv cloudflow.ps&

viewgv:
	ghostview cloudflow.ps

viewdvi:
	xdvi cloudflow.dvi&

r: 
	ghostview cloudflow.ps
	
