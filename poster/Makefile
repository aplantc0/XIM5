EDITOR = vim
file = poster

#all: compile clean compress

compile:
	latexmk -lualatex ${file}.tex
clean:
	latexmk -bibtex -c && find . -type f \( -name "*.snm" -o -name "*.nav" -o -name "*.blg" \) | xargs rm
compress:
	gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/prepress -dNOPAUSE -dQUIET -dBATCH -sOutputFile=${file}_comp.pdf ${file}.pdf


