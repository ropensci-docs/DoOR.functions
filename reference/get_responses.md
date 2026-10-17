# Find receptor responses

given a chemical, get original receptor responses from all studies in
the database.

## Usage

``` r
get_responses(
  odorant,
  responseRange = door_default_values("door_response_range"),
  Or.list = load2list()
)
```

## Arguments

- odorant:

  a single odor provided as InChIKey

- responseRange:

  data frame, response ranges of studies

- Or.list:

  a list contains reponse data of all available receptors. It can be
  loaded using
  [`load2list`](https://docs.ropensci.org/DoOR.functions/reference/load2list.md).

## Details

output is a data frame containing response values of given odor across
receptors from all available studies.

## Author

Daniel Münch <daniel.muench@uni-konstanz.de>

## Examples

``` r
# load data
library(DoOR.data)
load_door_data(nointeraction = TRUE)

# get raw responses for odorant MLFHJEHSLIIPHL-UHFFFAOYSA-N
responses <- get_responses(odorant = 'MLFHJEHSLIIPHL-UHFFFAOYSA-N')
```
