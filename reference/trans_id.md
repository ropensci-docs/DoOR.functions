# trans_id

Translate chemical identifiers from one to the other.

## Usage

``` r
trans_id(
  x,
  from = "CAS",
  to = "InChIKey",
  odor_data = door_default_values("odor")
)
```

## Arguments

- x:

  character vector, one or many chemical identifiers

- from:

  character, the type of identifier to translate from (one of the column
  names of “odor“)

- to:

  character, the type of identifier to translate from (one of the column
  names of “odor“)

- odor_data:

  the data frame containing the odor information (defaults to “odor“).

## Value

character vector of translated chemical identifiers

## Examples

``` r
# load data
library(DoOR.data)

# transform CAS to InChIKey
trans_id("123-92-2")
#> [1] "MLFHJEHSLIIPHL-UHFFFAOYSA-N"

# transform Name to InChIKey
trans_id("isopentyl acetate", "Name")
#> [1] "MLFHJEHSLIIPHL-UHFFFAOYSA-N"

# transform SMILE to InChIKey
trans_id("C(C(C)C)COC(=O)C", "SMILES", "Name")
#> [1] "isopentyl acetate"
```
