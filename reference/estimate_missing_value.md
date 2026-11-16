# Estimate the missing entries in a response data

Estimate the missing entries in a response data

## Usage

``` r
estimate_missing_value(data, nodor, method = "PC")
```

## Arguments

- data:

  a data frame or matrix, contaning the consensus response values

- nodor:

  a numeric value, specifying the number of the selected odors

- method:

  character string, specifying the method ("PC" (Pearson's coefficient)
  and "Knn" (k nearest neighbors)) for estimation, the default is "PC".

## Details

A wrapper programe for using Pearson Correlation or k-nearest neighbors
to estimate the missing entries in a response matrix.

## References

Kim, H., Golub, G. H. & Park, H., Missing value estimation for DNA
microarray gene expression data: local least squares imputation., 2005,
Bioinformatics, 21, 187-198

## Author

Shouwen Ma \<<shouwen.ma@uni-konstanz.de>\>

## Examples

``` r
if (FALSE) { # \dontrun{
# load data
library(DoOR.data)
data(door_response_matrix)

# pick an example subset
subset <- door_response_matrix[1:100, 11:30]

# estimate missing values
est.data <- estimate_missing_value(data = subset, nodor = 6)
} # }
```
