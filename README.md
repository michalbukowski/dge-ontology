# dge-ontology
DGE-ontology is a repository that provides solutions dedicated to: (1) performing
GSEA (gene set enrichment analysis/ontology analysis) on DGE (differential gene expression)
or similar results; (2) visualisation of integrated GSEA and DGE results in
one highly informative and visually appealing circular chart.

## Citing the software
The software is featured in the following publication:
Bukowski M and Wladyka B. (2024) _DGE-ontology: A quick and simple gene set enrichment analysis and visualisation tool_
SoftwareX [awaiting publication]

## Introduction
The software has been primarily designed for transcriptomics (for results
obtained using [Salmon](https://doi.org/10.1186/s13059-014-0550-8)<sup>1</sup>
and [DESeq2](https://doi.org/10.1038/nmeth.4197)<sup>2</sup>). However it may be
utilised for any data that express fold change of relative or absolute quantity
measures of multiple entities (transcripts, proteins, metabolites, etc.).

The software may be used in two ways:
- `dgeontology` library available from PyPI repository
- `DGE-ontology.ipynb` stand-alone Jupyter notebook

## The `dgeontology` library
The library is a good choice for those who expect to use the solution without
playing with the code interactively. The library installation and usage is
quite straightforward and described in details both on the library PyPI site
([here](https://pypi.org/project/dgeontology)) as well as in the
[dgeontology](https://github.com/michalbukowski/dge-ontology/tree/main/dgeontology) subdirectory
of this repository, where the library source is contained.

The library documentation provides a basic example its usage. Nevertheless, you
will find plenty of well-documented examples in Jupyter notebooks available in this
repository (see the next chapter).

## Jupyter notebooks
`DGE-ontology.ipynb` notebook contains the same code as the `dgeontology` library.
It allows not only to use the code in an interactive way but also to directly
modify and adapt it to the user&apos;s needs. Moreover, it provides a bit more
user-friendly (a bit less technical) documentation for the code.

`DGE-charts.ipynb` is an accessory notebook that facilitates a general analysis of
DGE results, such as: PCA (principal component analysis) of replicas based on
TPM values (transcripts per million), and creating TPM vs. TPM and volcano plots.

The last two notebooks, `dgeontology_basic_examples.ipynb` and `dgeontology_extra_examples.ipynb`,
provide examples of the `dgeontology` library usage that can be explored
interactively. The latter one includes, among all, visualisations used in the original
`DGE-ontology` publication in the SoftwareX (Elsevier) journal.

Each Jupyter notebook contains detailed step-by-step documentation and the methodology
description as well as the complete test output. If rerun for the exemplary input, exactly
the same results should be obtained. Selected visualisations are saved to the `output`
directory as high-resolution PNG files.

The exemplary input contains metadata on _Staphylococcus aureus_ RN4220 and USA300 FPR3757
transcriptomes and output from [rnaseq-pipeline-2](https://github.com/michalbukowski/rnaseq-pipeline-2)
executed for two pairs of strains: the wild type (`wt51e`) and &Delta;&Delta;_saoBC_ mutant (`mt51e`)
in the case of RN4220; and the wild type (`wt`) and &Delta;_saoC_ mutant (`mt`)
in the case of USA300 FPR3757, sampled in the logarithmic growth phase
(NCBI BioProject accession numbers PRJNA798259 and PRJNA1017382, respectively).

## Running the Jupyter notebooks
The content of all Jupyter notebooks can be accessed directly in a web browser from
this repository. However, in order to run the code
[Miniconda](https://docs.anaconda.com/free/miniconda/miniconda-other-installer-links/#linux-installers)
installation is required. The notebooks have been tested on Ubuntu 22.04 using
`conda` package manager 24.7.1 and the following packages:
 - jupyterlab 4.2.5
 - scikit-learn 1.5.1
 - scipy 1.14.1
 - pandas 2.2.2
 - matplotlib 3.9.2
as well as `pip` package manager 24.2 and the package:
 - dgeontology 1.0.0

A ready-to-use conda environment might be created using `envs/dge-ontology.yml`:
```bash
conda env create --file envs/dge-ontology.yml
```
When successfully created, the environment may be activated as following:
```bash
conda activate dge-ontology
```
Once the evironment is active, browse and run all of the notebooks in Jupyter Lab:
```bash
jupyter lab
```

#### References
1. [R. Patro, G. Duggal, M.I. Love, R.A. Irizarry, C. Kingsford, Nat. Methods 14 (2017) 417–419.](https://doi.org/10.1186/s13059-014-0550-8)<br>
2. [M.I. Love, W. Huber, S. Anders, Genome Biol. 15 (2014) 550.](https://doi.org/10.1038/nmeth.4197)
