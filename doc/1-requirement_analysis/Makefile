all:
	xelatex 1-requirement_analysis.tex
	makeglossaries 1-requirement_analysis
	xelatex 1-requirement_analysis.tex

clean:
	rm -f *.{aux,glg,glo,gls,glsdefs,ist,log,pdf,toc,out}

.PHONY: all clean
