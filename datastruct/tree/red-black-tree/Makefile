HEADER =
SOURCE = rbtree-en.tex
OBJECT = rbtree-en
TEX = xelatex

.PHONY: all

all: pdf

cpp:
	$(MAKE) cpp -C src

haskell:
	$(MAKE) haskell -C src

image:
	$(MAKE) -C img

pdf: $(OBJECT).dvi
	dvipdfmx $(OBJECT)

tex: pdf

pdf: image
	$(TEX) $(OBJECT)
	$(TEX) $(OBJECT)

html:
	htlatex $(OBJECT) "html, imgdir:img/"
	mv *.png img/

clean:
	rm -f *.4ct *.4tc *.aux *.css *.dvi *.html
	rm -f *.idv *.lg *.log *.out *.pdf *.tmp *.xref *.cache *.zip *~
