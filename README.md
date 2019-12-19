# Bayesian Causal Forests

Welcome to the `BCF` site! This page provides hands-on examples of how to conduct Bayesian causal forest (BCF) analyses. You can find methodological details on the underlying modeling approach in the original BCF paper: [Hahn, Murray, and Carvalho 2017](https://arxiv.org/pdf/1706.09523.pdf).

## Why BCF?

BCF is a cutting-edge causal inference methodology that builds on Bayesian Additive Regression Trees (BART, [Chipman, George, and McCulloch 2010](https://projecteuclid.org/euclid.aoas/1273584455)). More immediately, it builds on the application of BART to causal inference ([Hill 2011](https://www.tandfonline.com/doi/abs/10.1198/jcgs.2010.08162)).  BART and BCF both combine Bayesian regularization with regression trees to provide a highly flexible response surface that, thanks to the Bayesian regularizing priors, is not overfit to the training data.  BCF further extends BART's flexibility by specifying different models for relationships between (a) covariates and the outcome and (b) covariates and the treatment effect.

BCF performs remarkably well in simulation and has led the pack at recent rigorous causal inference competitions, such as those held at the Atlantic Causal Inference Conference. 

## Getting Started

If you are just getting started with BCF, we recommend starting with the tutorial vignettes on the "Articles" page of this website.

## Installation

This package requires compilation, so make sure you have Rtools properly installed -- details [here](https://cran.r-project.org/bin/windows/Rtools/).

Install the latest release from CRAN:

```{r}
install.packages("bcf")
```

Install the latest development version from GitHub:

```{r}
if (!require("devtools")) {
  install.packages("devtools")
}
devtools::install_github("jaredsmurray/bcf")
```