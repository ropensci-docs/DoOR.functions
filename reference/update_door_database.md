# update response matrix

update the globally `response matrix` and the unglobally normalized
response matrix `door_response_matrix_non_normalized` by introducing new
consensus response data of given receptor.

## Usage

``` r
update_door_database(
  receptor,
  permutation = TRUE,
  perm,
  response_matrix_nn = door_default_values("door_response_matrix_non_normalized"),
  response_matrix = door_default_values("door_response_matrix"),
  responseRange = door_default_values("door_response_range"),
  weightGlobNorm = door_default_values("door_global_normalization_weights"),
  select.MDValue = door_default_values("select.MDValue"),
  strict = TRUE,
  overlapValues = door_default_values("overlapValues"),
  door_excluded_data = door_default_values("door_excluded_data"),
  plot = FALSE
)
```

## Arguments

- receptor:

  character string, name of given odorant receptor.

- permutation:

  logical, if TRUE, the sequence is chosen from permutation, if FALSE,
  sequence is chosen by the routine process.

- perm:

  a matrix with one sequence of study names per row, if empty, all
  possible permutations of study names will be provided.

- response_matrix_nn:

  data frame, response data that has not been globally normalized.

- response_matrix:

  data frame, globally normalized response data.

- responseRange:

  data frame, response range of studies.

- weightGlobNorm:

  data frame, weight matrix for global normalization.

- select.MDValue:

  the minimum mean distance between studies to perfom a merge (used if
  permutation == FALSE or if permutation == TRUE AND strict == TRUE)

- strict:

  logical, if TRUE merging a permutation will be stopped once a single
  merge has a mean distance above select.MDValue (only valid if
  permutation == TRUE)

- overlapValues:

  minimum overlap between studies to perfom a merge

- door_excluded_data:

  the data frame that contains the list of excluded data sets.

- plot:

  logical

## Details

The merging sequence could be arranged by the routine process (using
[`model_response`](https://docs.ropensci.org/DoOR.functions/reference/model_response.md)
or taking the optimized sequence that is chosen from permutations. The
mean correlation between merged responses and each original recording
will be computed for each permutation, the optimozed sequence is with
the highest correlation.

## See also

[`model_response`](https://docs.ropensci.org/DoOR.functions/reference/model_response.md),[`model_response_seq`](https://docs.ropensci.org/DoOR.functions/reference/model_response_seq.md)

## Author

Shouwen Ma \<<shouwen.ma@uni-konstanz.de>\>

Daniel Münch \<<daniel.muench@uni-konstanz.de>\>

## Examples

``` r
if (FALSE) { # \dontrun{
# load data
library(DoOR.data)
load_door_data()
# update the entry "Or67b" of data "door_response_matrix" and
# "door_response_matrix_non_normalized" with permutations.
 update_door_database(receptor="Or67b", permutation = TRUE)
} # }
```
