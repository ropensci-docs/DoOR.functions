# compute the data pairwise and and selects a pair with the lowest "MD" value.

compute the data pairwise using function
[`calculate_model`](https://docs.ropensci.org/DoOR.functions/reference/calculate_model.md)
and selects a pair with the lowest "MD" value.

## Usage

``` r
select_model(
  candidate,
  data_candidate,
  merged_data,
  overlapValues = door_default_values("overlapValues"),
  merged = door_default_values("merged")
)
```

## Arguments

- candidate:

  a character vector, contains the names of studies.

- data_candidate:

  a data frame, odorant response data that only contains value columns.

- merged_data:

  numeric vector, merged data

- overlapValues:

  numeric, a criterion using to refuse a data set that has not enough
  overlap value.

- merged:

  logical, if merged is `TRUE`, calculate models between merged_data and
  candidate data. If `FALSE`, calculate models between candidates.

## Details

This function is used in
[`model_response`](https://docs.ropensci.org/DoOR.functions/reference/model_response.md)
to select the first pair or next data set for merging. The output is a
list containing "selected.x" and "selected.y" that specify which data
plots against another, and "best.model" that is used in function
[`project_points`](https://docs.ropensci.org/DoOR.functions/reference/project_points.md).

## See also

[`project_points`](https://docs.ropensci.org/DoOR.functions/reference/project_points.md),[`model_response`](https://docs.ropensci.org/DoOR.functions/reference/model_response.md)

## Author

Shouwen Ma \<<shouwen.ma@uni-konstanz.de>\>

## Examples

``` r
# load data
library(DoOR.data)
data(ac3B)

# split into data and header
studies <- names(ac3B)[c(7:8)]
data_candidate <- ac3B[,c(7:8)]

# rescale data
norm_data_candidate <- apply(data_candidate, 2, door_norm)

# find the best fitting model
select_model(candidate = studies, data_candidate = norm_data_candidate,
             merged = FALSE)
#> $best.model
#> $best.model$initial
#> $best.model$initial$model.name
#> [1] "no.fitted.model"
#> 
#> $best.model$initial$cal.parameters
#> [1] NA
#> 
#> $best.model$initial$MD
#> [1] 0.1415
#> 
#> 
#> 
#> $selected.x
#> character(0)
#> 
#> $selected.y
#> character(0)
#> 
```
