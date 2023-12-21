# Makefile pour la documentation Sphinx

# Répertoire source où se trouvent les fichiers .rst
SPHINX_SOURCE = src

# Répertoire de sortie où les fichiers HTML seront générés
SPHINX_BUILD = _build

# Commande Sphinx
SPHINXBUILD = sphinx-build

# Options de sphinx-build
SPHINXOPTS =

# Mettez vos options de make ici (ou laissez vide par défaut)
ALLSPHINXOPTS = -d $(SPHINX_BUILD)/doctrees $(SPHINXOPTS) $(SPHINX_SOURCE)

# Règle par défaut
all: html

# Règle pour générer la documentation HTML
html:
	@$(SPHINXBUILD) -b html $(ALLSPHINXOPTS) $(SPHINX_BUILD)/html

# Règle pour générer la documentation en format LaTeX
latex:
	@$(SPHINXBUILD) -b latex $(ALLSPHINXOPTS) $(SPHINX_BUILD)/latex

# Règle pour compiler les fichiers LaTeX en PDF
pdf: latex
	@make -C $(SPHINX_BUILD)/latex all-pdf

latexpdf:
	$(SPHINXBUILD) -b latex $(ALLSPHINXOPTS) $(SPHINX_BUILD)/latex
	@echo "Running LaTeX files through pdflatex..."
	$(MAKE) -C $(SPHINX_BUILD)/latex all-pdf


# Règle pour nettoyer les fichiers générés
clean:
	@rm -rf $(SPHINX_BUILD)/

# Autres règles pour différentes sorties (comme PDF, ePub, etc.) peuvent être ajoutées ici
