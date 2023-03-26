# dge-ontology
Two Jupyter notebooks that aim at visualising DGE results obtained using Salmon and DESeq2 as well as at performing ontology analysis and visualisation for these results. The exemplary input contains metadata on _Staphylococcus aureus_ RN4220 transcriptome and output from [rnaseq-pipeline-2](https://github.com/michalbukowski/rnaseq-pipeline-2) executed for two strains sampled in the logarithmic growth phase: a wild type (`wt_lg`) vs. $\Delta$_saoC_ mutant (`mt_lg`).

Notebook cell output has been saved in the original (repository) version of the notebooks. If rerun for the exemplary data, the same results should be obtained. All visualisations are saved to `output` directory as high-resolution PNG files.

## Environment setup
Miniconda or Anaconda installation is required. The notebooks have been tested using the following packages:
* python 3.11.0 
* numpy 1.24.2
* pandas 1.5.3
* matplotlib 3.7.1
* scipy 1.10.1
* scikit-learn 1.2.2 
* jupyterlab 3.5.0
* pillow 9.4.0

A ready-to-use conda environment might be created from `conda/dge-ontology.txt` file:
```bash
conda create -n dge-ontology --file conda/dge-ontology.txt
```
When successfully created, the environment may be activated:
```bash
conda activate dge-ontology
```
The notebooks can be now browsed and run in Jupyter Lab:
```bash
jupyter lab
```
