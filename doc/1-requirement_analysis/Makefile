ASSIGNMENT = 1-requirement_analysis

all: pdf

pdf:
	@xelatex ${ASSIGNMENT}.tex
	@makeglossaries ${ASSIGNMENT}
	@xelatex ${ASSIGNMENT}.tex

html:
	@pandoc --resource-path=img \
		--self-contained \
		-c https://levendula.bertalanp99.eu/css/style.css \
		-o ${ASSIGNMENT}.html \
		${ASSIGNMENT}.tex

clean:
	rm -f *.{html,pdf}
	rm -f *.{aux,log,out}
	rm -f *.{glg,glo,gls,glsdefs}
	rm -f *.lof
	rm -f *.ist

.PHONY: all clean
