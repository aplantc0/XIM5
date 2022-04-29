EDITOR = vim
1 = abstract

all: pdf docx
pdf:
	pandoc ${1}.md --pdf-engine=lualatex -V documentclass=article -V papersize=a4 -V geometry:margin=3.5cm -V classoption=onecolumn -V mainfont='CMU Serif' -V fontsize=10pt -V lang=en -o ${1}.pdf
docx:
	pandoc ${1}.md --pdf-engine=lualatex -V documentclass=article -V papersize=a4 -V geometry:margin=3.5cm -V classoption=onecolumn -V mainfont='CMU Serif' -V fontsize=10pt -V lang=en -o ${1}.docx



