EDITOR = vim
file = poster

.PHONY: compile clean 

compile:
	latexmk -lualatex ${file}.tex
clean:
	latexmk -bibtex -c && find . -type f \( -name "*.snm" -o -name "*.nav" -o -name "*.blg" \) | xargs rm
