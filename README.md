IQKM
==========

This project provides tools for Integrated Quantile Kernel Machine for testing microbiome-outcome association.


Usage
-----
Suppose you have a sample dataset stored in a list with Y = SampleData$y, covriates C = SampleData$c, OTU data X = SampleData$x.

``` r
library(GUniFrac)
library(cluster)
library(dirmult)
library(MiRKAT)
library(MASS)
library(quadprog)
library(quantreg)
library(PearsonDS)
library(SKAT)

# run the iQKM
D.BC= as.matrix(vegdist(X, method="bray"))
K.BC= D2K(D.BC) # you can also use other K matrices.
IQKM(Y, C, K = K.BC)
```

License
-------

This package is free and open source software, licensed under GPL (&gt;=2).
