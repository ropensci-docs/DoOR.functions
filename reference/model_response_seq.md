# model_response_seq

generates a model response and merge data in given sequence

## Usage

``` r
model_response_seq(
  data,
  SEQ,
  overlapValues = door_default_values("overlapValues"),
  select.MDValue = door_default_values("select.MDValue"),
  strict = TRUE,
  plot = FALSE
)
```

## Arguments

- data:

  data frame, odorant response data, e.g. Or22a.

- SEQ:

  character vector, containing the names of studies indicating given
  sequence for merging data.

- overlapValues:

  minimum overlap between studies to perfom a merge

- select.MDValue:

  the minimum mean distance between studies to perfom a merge

- strict:

  logical, if TRUE merging a permutation will be stopped once a single
  merge has a mean distance above select.MDValue

- plot:

  logical

## Details

\# model_response_seq.R: \#################

\# merges studies in a given sequence (determined by the user or by
exhaustive enumeration and choosing the optimal sequence)

\# input parameters: \####################

\# data : data frame, odorant response data for a given receptor, e.g.
Or22a \# SEQ : character vector, contains the names of studies that
measured this receptor in a specific order (the merging sequence)

\# output is a numeric vector: response values

## Author

Shouwen Ma \<<shouwen.ma@uni-konstanz.de>\>

## Examples

``` r
# load data
library(DoOR.data)
data(Or35a)
data(door_response_range)

# specify a sequence of merging
SEQ <- c("Hallem.2006.EN","Kreher.2008.EN","Hallem.2006.EN")

# perform the merging
selected_merg <- model_response_seq(Or35a, SEQ = SEQ, plot = TRUE)
#> Warning: selfStart initializing functions should have a final '...' argument since R 4.1.0
#> Warning: selfStart initializing functions should have a final '...' argument since R 4.1.0
#> Warning: selfStart initializing functions should have a final '...' argument since R 4.1.0
#> Warning: selfStart initializing functions should have a final '...' argument since R 4.1.0

```
