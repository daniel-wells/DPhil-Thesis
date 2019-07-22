# Daniel Wells DPhil Thesis

mkdir aux_fikes
pdflatex -synctex=1 -interaction=nonstopmode -output-directory=compiled %.tex
biber % --output_directory=compiled

git clone --bare

git clone --bare git@github.com:mcmanigle/OxThesis.git DPhilThesis

git push --mirror https://github.com/daniel-wells/DPhil-Thesis.git
