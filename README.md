# Daniel Wells DPhil Thesis

Download the compiled version at the [ORA](https://ora.ox.ac.uk/objects/uuid:8c1f75a8-ecc3-4ffe-b01f-d2e92c75e66c)

## Setup
This latex template is from https://github.com/mcmanigle/OxThesis
```{bash}
git clone --bare https://github.com/mcmanigle/OxThesis.git
cd OxThesis.git

git push --mirror ssh://git@github.com/daniel-wells/DPhil-Thesis.git
cd ..
rm -rf OxThesis.git

git clone ssh://git@github.com/daniel-wells/DPhil-Thesis.git
```

Compared to the forked project I needed to change include command to input.

## Compilation
```{bash}
mkdir compiled
pdflatex -synctex=1 -interaction=nonstopmode -output-directory=compiled %.tex
biber % --output_directory=compiled
pdflatex -synctex=1 -interaction=nonstopmode -output-directory=compiled %.tex
```
Note to self: remember to change log file location in texstudio and the Bibliography is automatically exported from zotero.

