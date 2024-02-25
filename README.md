# dge-ontology
DGE-ontology is a set of two Jupyter notebooks dedicated to:
 - visualisation of differential gene expression (DGE) analysis results
 - gene set enrichment analysis (ontology analysis) and visualisation

## Introduction
The software has been primarily designed for transcriptomics (for results
obtained using Salmon<sup>1</sup> and DESeq2<sup>2</sup>), however it may be
utilised for any data that express fold change of relative or absolute quantity
measures of multiple entities (transcripts, proteins, metabolites, etc.).

Detailed step-by-step documentation and the methodology description are placed
in both notebooks.

The exemplary input contains metadata on _Staphylococcus aureus_ RN4220
transcriptome and output from [rnaseq-pipeline-2](https://github.com/michalbukowski/rnaseq-pipeline-2)
executed for two strains: wild type (`wt51e`) and &Delta;&Delta;_saoBC_ mutant (`mt51e`).

Notebooks contain the test output. If rerun for the exemplary input, exactly
the same results should be obtained. All visualisations are saved to `output`
directory as high-resolution PNG files.

## Environment setup
[Miniconda](https://docs.anaconda.com/free/miniconda/miniconda-other-installer-links/#linux-installers)
installation is required. The notebooks have been tested on Ubuntu 22.04 using
conda package manager 23.11.0 and the following packages:
 - jupyterlab 4.0.11
 - scikit-learn 1.4.0
 - scipy 1.12.0
 - pandas 2.2.0
 - matplotlib 3.8.2
 - pillow 10.2.0
 - pyarrow 14.0.2

A ready-to-use conda environment might be created using `envs/dge-ontology.yml`:
```bash
conda env create --file envs/dge-ontology.yml
```
When successfully created, the environment may be activated as follwing:
```bash
conda activate dge-ontology
```
Once the evironment is active, browse and run the notebooks in Jupyter Lab:
```bash
jupyter lab
```

#### References
1. [R. Patro, G. Duggal, M.I. Love, R.A. Irizarry, C. Kingsford, Nat. Methods 14 (2017) 417–419.](https://doi.org/10.1186/s13059-014-0550-8)<br>
2. [M.I. Love, W. Huber, S. Anders, Genome Biol. 15 (2014) 550.](https://doi.org/10.1038/nmeth.4197)
