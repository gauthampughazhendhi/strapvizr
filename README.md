
<!-- README.md is generated from README.Rmd. Please edit that file -->

# StrapvizR

<!-- badges: start -->
<!-- badges: end -->

## Summary

Performs bootstrapping of a sample to produce plots and statistics for
use in final reports and documents.

The purpose of this package is to simplify and automate the process of
creating simple bootstrap distributions of numerical samples. The
package has a module which intakes a sample and relevant parameters such
as the desired confidence bounds and number of simulations. The module
will perform the simulation statistics to generate the bootstrap
distribution and relevant statistics such as the sample mean and
bootstrapped confidence interval. The package also has a module for
visualization of the bootstraped confidence interval, and for creating a
professional publication-ready table of the relevant statistics.

## Package context within the R ecosystem

The package builds on the
[dplyr](https://cran.r-project.org/web/packages/dplyr/) package and the
[ggplot2](https://cran.r-project.org/web/packages/ggplot2/) package to
achieve the above mentioned functionalities. The
[BootCI](https://rdrr.io/cran/DescTools/man/BootCI.html) package seems
to streamline the confidence interval process but does not include
plotting support. **StrapvizR** streamlines the process of bootstrapping
from data to visualization and embedding in documents which is not
available as a single bundle. Some tutorials on bootstrap confidence
intervals at sources
[(1)](https://moderndive.com/8-confidence-intervals.html),
[(2)](http://pages.stat.wisc.edu/~larget/stat302/chap3.pdf) and
[(3)](https://www.geeksforgeeks.org/bootstrap-confidence-interval-with-r-programming/)
encourage the reader to plot the results manually.

## Installation

You can install the released version of `strapvizr` from
[CRAN](https://CRAN.R-project.org) with:

``` r
install.packages("strapvizr")
```

And the development version from [GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("UBC-MDS/strapvizr")
```

## Example

This is a basic example which shows you how to solve a common problem:

``` r
# library("strapvizr")
# plot_ci([1, 2, 3, 4, 5, 6, 7], 1000, n = 100, ci_level = 0.95, ci_random_seed = 123)
```

## Function Usage

-   `bootstrap_distribution`: Returns a sampling distribution of
    specified replicates is generated for a specified estimator with
    replacement for a given bootstrap sample size.

-   `calculate_boot_stats`: Calculates a confidence interval for a given
    sampling distribution as well as other bootstrapped statistics.

-   `plot_ci`: Creates a histogram of a bootstrapped sampling
    distribution with its confidence interval and observed sample
    statistic.

-   `tabulate_stats`: Generates a table that contains a given sampling
    distribution’s mean and standard deviation along with relevant
    statistics as well as a summary table of the bootstrap distributions
    parameters. The code automatically saves the tables as html
    documents.

## Contributing

Julien Gordon, Gautham Pughazhendhi, Zack Tang, and Margot Vore.

## License

\`StrapvizR\` was created by Julien Gordon, Gautham Pughazhendhi, Zack
Tang, Margot Vore. It is licensed under the terms of the MIT license.
