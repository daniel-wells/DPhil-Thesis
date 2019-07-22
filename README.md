# Daniel Wells DPhil Thesis

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

## Compilation
```{bash}
mkdir compiled
pdflatex -synctex=1 -interaction=nonstopmode -output-directory=compiled %.tex
biber % --output_directory=compiled
pdflatex -synctex=1 -interaction=nonstopmode -output-directory=compiled %.tex
```