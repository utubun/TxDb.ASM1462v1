
# TxDb.Paeruginosa.PA14

<!-- badges: start -->
[![Lifecycle: experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://lifecycle.r-lib.org/articles/stages.html#experimental)
<!-- badges: end -->

Annotation package for *Pseudomonas aeruginosa* str. PA14. Data source: [NCBI](https://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/000/014/625/GCF_000014625.1_ASM1462v1/)

## Installation

You can install the development version of TxDb.Paeruginosa.PA14 like so:

``` r
devtools::install_github('utubun/TxDb.Paeruginosa.PA14')
```

## Example

This is a basic example which shows you how to solve a common problem:

``` r
library(TxDb.Paeruginosa.PA14)

pa14tx <- TxDb.Paeruginosa.PA14

# show the information related to the build
pa14tx

# extract genes, as genomic ranges
gr <- GenomicFeatures::genes(pa14tx)

# show extracted ranges
gr

# convert gene ID into transcript names
head(
  (nm <- biomaRt::select(pa14tx, names(gr), 'TXNAME', 'GENEID')
)
```

## More examples

``` r
methods(class = class(pa14tx))

help(package = 'GenomicFeatures')
```

