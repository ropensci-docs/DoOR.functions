# Find normalised receptor responses

given a chemical, get normalised receptor responses from all studies in
the database.

## Usage

``` r
get_normalized_responses(
  odors,
  zero = door_default_values("zero"),
  response_matrix = door_default_values("door_response_matrix"),
  round = 3,
  na.rm = FALSE
)
```

## Arguments

- odors:

  character vector, one or more odors provided as InChIKey.

- zero:

  InChIKey of background that should be set to zero. The default is
  "SFR", i.e. the spontaneous firing rate.

- response_matrix:

  a data frame, as e.g. "door_response_matrix" that is loaded by
  [`model_response`](https://docs.ropensci.org/DoOR.functions/reference/model_response.md).
  It is also possible to create this frame manually using
  [`model_response`](https://docs.ropensci.org/DoOR.functions/reference/model_response.md).

- round:

  numeric, round to this amount of digits, set to NA if you do not want
  to round

- na.rm:

  logical, remove NAs?

## See also

[`model_response`](https://docs.ropensci.org/DoOR.functions/reference/model_response.md),[`create_door_database`](https://docs.ropensci.org/DoOR.functions/reference/create_door_database.md)

## Author

Daniel Münch <daniel.muench@uni-konstanz.de>

## Examples

``` r
# load data
library(DoOR.data)
data(door_response_matrix)

# define a list of odorants
odors <- c("MLFHJEHSLIIPHL-UHFFFAOYSA-N",
           "OBNCKNCVKJNDBV-UHFFFAOYSA-N",
           "IKHGUXGNUITLKF-UHFFFAOYSA-N")

# get the normalized responses for these odorants
result <- get_normalized_responses(odors, 
                                   response_matrix = door_response_matrix)
```
