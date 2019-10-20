ASSIGNMENT = 2-structural_modelling

all: pdf

pdf:
	@xelatex ${ASSIGNMENT}.tex
	@makeglossaries ${ASSIGNMENT}
	@xelatex ${ASSIGNMENT}.tex

# XXX: do NOT modify HTML with sed! I am just lazy… -- bertalanp99
html:
	@pandoc --standalone \
		-c https://levendula.bertalanp99.eu/css/style.css \
		-o ${ASSIGNMENT}.html \
		${ASSIGNMENT}.tex
	@sed -i 's|src="\(.*\.jpg\)"|src="img/\1"|g' ${ASSIGNMENT}.html
	@sed -i 's|src="\(.*\.png\)"|src="img/\1"|g' ${ASSIGNMENT}.html
	@sed -i 's/<img/<img width="100%"/g' ${ASSIGNMENT}.html

clean:
	rm -f *.{html,pdf}
	rm -f *.{aux,log,out}
	rm -f *.{glg,glo,gls,glsdefs}
	rm -f *.toc
	rm -f *.lof
	rm -f *.ist

.PHONY: all clean
