EDITOR = vim
file = poster

compile:
	latexmk -lualatex ${file}.tex
clean:
	latexmk -bibtex -c && find . -type f \( -name "*.snm" -o -name "*.nav" -o -name "*.blg" \) | xargs rm
compress:
	gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/printer -dNOPAUSE -dQUIET -dBATCH -sOutputFile=${file}_comp.pdf ${file}.pdf
jpg:
	pdftoppm -jpeg -r 300 -singlefile ${file}_comp.pdf ${file} && mogrify -verbose -strip -quality 10 ${file}.jpg
all: compile clean compress jpg
