# Delineation of meiotic gene expression in male mice
### DPhil Thesis by Daniel Wells

Download the compiled version from the [GitHub release](https://github.com/daniel-wells/DPhil-Thesis/releases/tag/v1.0) or from the [Oxford Research Archive](https://ora.ox.ac.uk/objects/uuid:8c1f75a8-ecc3-4ffe-b01f-d2e92c75e66c).

## Abstract
Meiosis is a specialised cell division producing the haploid gametes required for sexual reproduction. A key function of this process is to generate genetic diversity through recombination and independent assortment of homologous chromosomes. Delineation of gene expression during this process has been challenging due to the heterogeneity of testis tissue and the lack of faithful _in vitro_ models.

Here we jointly analyse a single-cell resolution transcriptomic dataset of over 20,000 cells from both wild type and mutant mice. We use dimensionality reduction methods to infer latent components of variation that represent transcriptional programmes, mutant specific pathological processes, and technical effects. This approach simultaneously soft clusters cells, infers corresponding groups of co-expressed marker genes, and imputes sparse, noisy gene expression. We were also able to infer, _de novo_, transcription factor binding motifs for each component, revealing a general switch at the meiotic divisions. We facilitate access to this resource by providing an interactive website [testisatlas.ml](http://www.testisatlas.ml).

The high-resolution delineation of gene expression during the spermatogenic programme provides high-resolution clues to the function of understudied genes. One such gene, _Zcwpw1_, is highly co-expressed with _Prdm9_, and has domains capable of recognising the unique combination of histone marks that PRDM9 deposits (H3K4me3 and H3K36me3). By using a human _in vitro_ system of _Zcwpw1_ co-transfection with either human or chimp _Prdm9_, we show that PRDM9 causes the recruitment of ZCWPW1 to its binding sites. This recruitment is stronger than for sites with H3K4me3 alone and is CpG dependent.

Male _Zcwpw1<sup>-/-</sup>_ mice have completely normal double strand break positioning, but severe repair and synapsis defects leading to complete testicular azoospermia. Although PRDM9’s effect of DSB positioning remains intact, PRDM9’s effect of aiding synapsis appears to be abolished, with persistent DMC1 signal - most dramatically at the most strongly PRDM9 bound hotspots.

## Citation
Please cite using the following BibTex entry:

```
@phdthesis{wells2020delineation,
   author = {Wells, Daniel},
   institution = {University of Oxford},
   publisher = {University of Oxford Research Archive},
   title = {Delineation of meiotic gene expression in male mice},
   year = {2020},
   url = {https://ora.ox.ac.uk/objects/uuid:8c1f75a8-ecc3-4ffe-b01f-d2e92c75e66c}
}
```

## Related Publications
* _ZCWPW1 is recruited to recombination hotspots by PRDM9, and is essential for meiotic double strand break repair_
**Daniel Wells**, Emmanuelle Bitoun, Daniela Moralli, Gang Zhang, Anjali Hinch, Julia Jankowska, Peter Donnelly, Catherine Green, Simon R Myers. *eLife* (2020). [`DOI: doi.org/10.7554/eLife.53392`](https://doi.org/10.7554/eLife.53392) [`Code: github.com/myersgroup/Zcwpw1`](https://github.com/myersgroup/Zcwpw1)

* _Unified single-cell analysis of testis gene regulation and pathology in five mouse strains_
Min Jung, **Daniel Wells**, Janette Rusch, Suhaira Ahmed, Jonathan Marchini, Simon R Myers, Donald Conrad. *eLife* (2019). [`DOI: doi.org/10.7554/eLife.43966`](https://doi.org/10.7554/eLife.43966) [`Code: github.com/myersgroup/testisAtlas`](https://github.com/myersgroup/testisAtlas)


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

