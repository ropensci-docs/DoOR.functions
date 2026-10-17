# Compose a Response Matrix of All Odor Receptors

computes the complete response model for all receptors in the database
(calls
[`model_response`](https://docs.ropensci.org/DoOR.functions/reference/model_response.md)
for all receptors). Overwrites response_matrix,
door_response_matrix_non_normalized and door_excluded_data.

## Usage

``` r
create_door_database(
  tag = door_default_values("tag"),
  select.MDValue = door_default_values("select.MDValue"),
  overlapValues = door_default_values("overlapValues"),
  ...
)
```

## Arguments

- tag:

  character string, format for rownames, possibilities: "InChIKey",
  CAS", "CID", "Name"

- select.MDValue:

  a numeric, threshold on the MD, this is used to reject studies that do
  not align sufficiently well to the response model

- overlapValues:

  numeric, a criterion using to refuse a data set that has not enough
  overlap value.

- ...:

  pass more parameters to
  [`model_response`](https://docs.ropensci.org/DoOR.functions/reference/model_response.md)

## See also

[`model_response`](https://docs.ropensci.org/DoOR.functions/reference/model_response.md)

## Author

Shouwen Ma \<<shouwen.ma@uni-konstanz.de>\>

Daniel Münch \<<daniel.muench@uni-konstanz.de>\>

## Examples

``` r
if (FALSE) { # \dontrun{
# load DoOR data
library(DoOR.data)
load_door_data()

# create a new consensus matrix
create_door_database()
} # }
```
