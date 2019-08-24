# Data prepration

This folder contains instructions on how to reproduce the results found in the "GTEX data analysis" section of [the paper](https://arxiv.org/abs/1811.01076).

Some files are too big for github and must be downloaded seperately.

You can either 

- use the already processed data, in which case you have nothing to do:

   - `all_tissues.preprocessed.data.RData.gz` (this file should be readable by R) contains the expression and covariates in a format which is convenient for our analyses. Download it to this directory from [Google Drive](https://drive.google.com/open?id=14xqCMZHuJ1OMpRd0FwISXWmA42CSMpnW)
   - `gencode.v19.genes.v7.patched_contigs.gtf` : A release of the GENCODE annotations. See [https://www.gencodegenes.org/human/release_19.html](https://www.gencodegenes.org/human/release_19.html). This is used to identify protein coding genes: we run the analysis on those only. Download it to this directory from [Google Drive](https://drive.google.com/open?id=1XCIQn-iAH7TRlmIdll1RT9ZIZ7lzaZ9j)
   - `gene_name_mapping.csv` : A file which maps gene names to their ensembl ID.
- prepare the data yourself by downloading it from the GTEX consortium and running the script `prepare_all_datasets.R`.

The steps are as follows:
  - 1. Download the gene expression data from the GTEX website. See below.
  - 2. Run the script `prepare_all_datasets.R` . This will create two files: `all_tissues.preprocessed.data.RData.gz`  and `gene_name_mapping.csv` . 
    - To run the script, make sure you have the `hash` [R package](https://cran.r-project.org/web/packages/hash/index.html).
    - Run : `R --no-save < prepare_all_datasets.R` .

## Download the GTEX gene expression data

We used the V7 version of the data. You should downloaded the following files from [the GTEX website](https://gtexportal.org/home/datasets) and extract them in this folder:

-  [GTEx_Analysis_v7_eQTL_expression_matrices.tar.gz](https://storage.googleapis.com/gtex_analysis_v7/single_tissue_eqtl_data/GTEx_Analysis_v7_eQTL_expression_matrices.tar.gz) . Extracting this file will create a directory with 96 files with names like: `"Colon_Transverse.v7.normalized_expression.bed.gz"` and `"Colon_Transverse.v7.normalized_expression.bed.gz.tbi"`.
-  [GTEx_Analysis_v7_eQTL_covariates.tar.gz](https://storage.googleapis.com/gtex_analysis_v7/single_tissue_eqtl_data/GTEx_Analysis_v7_eQTL_covariates.tar.gz). This will create a directory with 48 files with names like: `"Colon_Transverse.v7.covariates.txt"`. 
