# stac.R
R Client Library for SpatioTemporal Asset Catalog (STAC)


STAC is a specification of files and web services used to describe geospatial information assets.
The specification can be consulted in [https://stacspec.org/].

STAC client for R (`stac`) was designed to fully support STAC v0.8.0. 
As STAC spec is evolving fast and reaching its maturity, we plan update `stac` to support upcoming STAC 1.0.0 version.

## installation

To install `stac` for R, the following commands 

```R
library(devtools)
install_github("brazil-data-cube/stac.R")
```

## usage

In this version, we only implemented STAC endpoints (`'/stac'` and `'/stac/search'`) functions.

```R
library(stac)

stac("http://brazildatacube.dpi.inpe.br/bdc-stac/0.8.0")
stac_search(url = "http://brazildatacube.dpi.inpe.br/bdc-stac/0.8.0",
            collections = "MOD13Q1",
            bbox = c(-55.16335, -4.26325, -49.31739, -1.18355))
```