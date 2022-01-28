
<!-- README.md is generated from README.Rmd. Please edit that file -->

# strapr

<!-- badges: start -->
<!-- badges: end -->

## Summary

Performs bootstrapping of a dataset column to produce plots and
statistics for use in final reports and documents.

The purpose of this package is to simplify and automate the process of
creating simple bootstrap distributions of numerical data columns. The
package will have a module which intakes a dataset column and relevant
parameters such as the desired confidence bounds and number of
simulations. The module will perform the simulation statistics to
generate the bootstrap mean distribution and relevant statistics such as
the sample mean and bootstrapped confidence interval. The package will
also contain a module for visualization of the bootstraped confidence
interval, and a module for creating a professional publication-ready
table of the relevant statistics.

## **Package context within the R ecosystem**

The package will likely build on the [infer
package](https://cran.r-project.org/web/packages/infer/index.html) or
the [boot package](https://cran.r-project.org/web/packages/boot/), which
allows one to conduct the bootstrap sampling in the first place using
the generate() and boot() functions. strapr will streamline and extend
this process from the pure statistical process done in this module. The
[BootCI](https://rdrr.io/cran/DescTools/man/BootCI.html) package seems
to streamline the confidence interval process but does not include
plotting support. While we cannot be certain that one does not exist,
there does not seem to be a package which streamlines the process from
data to visualization and presentation as proposed in this document.
Some tutorials on bootstrap confidence intervals at
<https://moderndive.com/8-confidence-intervals.html>,
<http://pages.stat.wisc.edu/~larget/stat302/chap3.pdf> and
<https://www.geeksforgeeks.org/bootstrap-confidence-interval-with-r-programming/>
encourage the reader to plot the results manually.

## Installation

You can install the released version of strapr from
[CRAN](https://CRAN.R-project.org) with:

``` r
install.packages("strapr")
```

And the development version from [GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("UBC-MDS/strapr")
```

## Example

This is a basic example which shows you how to solve a common problem:


``` r
# library("strapR")
# plot_ci([1, 2, 3, 4, 5, 6, 7], 1000, n = 100, ci_level = 0.95, ci_random_seed = 123)
```

## Function Usage

-   bootstrap_distribution: A sampling distribution of \`rep\`
    replicates is generated for a specified estimator with replacement
    for a given bootstrap sample size.

-   calculate_boot_stats: A confidence interval for a given sampling
    distribution is calculated for a given confidence level. The
    interval and other statistics relevant to the distribution and its
    creation are returned in a dictionary.

-   plot_ci: Plots a bootstrapped sampling distribution with
    its confidence interval and observed mean.

-   tabulate_stats: Generates two tables contains the sampling
    distribution’s statistics and the parameters of the bootstrapping
    method.

## Contributing

Julien Gordon, Gautham Pughazhendhi, Zack Tang, and Margot Vore.

## License

\`strapr\` was created by Julien Gordon, Gautham Pughazhendhi, Zack
Tang, Margot Vore. It is licensed under the terms of the MIT license.
