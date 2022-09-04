EDITOR = vim
file = poster

.PHONY: compile clean 

compile:
	latexmk -lualatex ${file}.tex # -pdf
clean:
	latexmk -bibtex -c # && find . -type f \( -name "*.xml" -o -name "*.bbl" -o -name "*.blg" \) | xargs rm
