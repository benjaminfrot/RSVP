# RSVP
Code for [RSVP-graphs: Fast High-dimensional Covariance Matrix Estimation under Latent Confounding](https://arxiv.org/abs/1811.01076) .

## Code and tutorial

The R notebook [RSVP_Example.ipynb](https://github.com/benjaminfrot/RSVP/blob/master/RSVP_Example.ipynb) contains
R code to implement both RSVP and RSVP-sub. 
The notebook shows how to:
  - 1 Implement RSVP and RSVP-sub in R;
  - 2 Estimate a graph by ranking the entries of the estimated covariance matrix;
  - 3 Use it in combination with neighbourhood selection to estimate an undirected graphical model.
  
 ## Application code and dataset
 
 The "GTEX data analysis" section of [RSVP-graphs: Fast High-dimensional Covariance Matrix Estimation under Latent Confounding](https://arxiv.org/abs/1811.01076) describes an application of RSVP to gene expression data generated
by the [GTEX consortium](https://gtexportal.org/home/). The [DataAnalysis](https://github.com/benjaminfrot/RSVP/tree/master/DataAnalysis) folder contains more information on how to reproduce the results of the paper.
