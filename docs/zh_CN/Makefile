# Minimal makefile for Sphinx documentation
#

# You can set these variables from the command line, and also
# from the environment for the first two.
SPHINXOPTS    ?=
SPHINXBUILD   ?= sphinx-build
SOURCEDIR     = source
BUILDDIR      = build

# Put it first so that "make" without argument is like "make help".
help:
	@$(SPHINXBUILD) -M help "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

.PHONY: help Makefile

# Catch-all target: route all unknown targets to Sphinx using the new
# "make mode" option.  $(O) is meant as a shortcut for $(SPHINXOPTS).
%: Makefile
	@$(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

view:
	google-chrome build/html/index.html

apidoc:
	sphinx-apidoc -f -o source/_module ../../../ultraopt
	rm source/_module/setup.rst

cp_tutorial:
	mkdir  -p source/_tutorials
	cp -r ../../tutorials_zh/*.ipynb source/_tutorials/
#	cp -r ../../tutorials_zh/README.md source/tutorial.md

cp_readme:
	cp -r ../../README.zh_CN.md source/introduction.md