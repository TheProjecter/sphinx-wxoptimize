# Test makefile for sample rst files

SPHINXOPTS    =
SPHINXBUILD   = sphinx-build
BUILDDIR      = _build
ALLSPHINXOPTS   = -d $(BUILDDIR)/doctrees $(SPHINXOPTS) .

.PHONY: htmlhelp

htmlhelp:
	$(SPHINXBUILD) -b htmlhelp $(ALLSPHINXOPTS) $(BUILDDIR)/htmlhelp
	mkdir -p $(BUILDDIR)/htmlhelp-converted
	-rm -rf $(BUILDDIR)/htmlhelp-converted/*
	../sphinx-wxoptimize $(BUILDDIR)/htmlhelp -o $(BUILDDIR)/htmlhelp-converted

viewold:
	helpviewer $(BUILDDIR)/htmlhelp/testdoc.hhp

viewnew:
	helpviewer $(BUILDDIR)/htmlhelp-converted/testdoc.hhp

clean:
	-rm -rf $(BUILDDIR)/*
