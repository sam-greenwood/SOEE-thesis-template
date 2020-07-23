latex=pdflatex
bib=biber

main_file=0_thesis
aux_files=.xml .aux .bbl .blg .log .lof .idx .bcf .toc .out .fdb_latexmk .fls .qz .ilg .nlo .nls


compile: build tidy

build: ${main_file}.tex
	${latex} ${main_file}.tex
	${bib} ${main_file}
	makeindex ${main_file}.nlo -s nomencl.ist -o ${main_file}.nls
	${latex} ${main_file}.tex

tidy:
	mkdir -p auxillary_files
	for f in ${aux_files}; do mv *$${f} auxillary_files/; done

remove:
	rm -rf ./auxillary_files

clean: tidy remove

