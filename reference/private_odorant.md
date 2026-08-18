# private_odorant

return an odorant that activates the receptor of interest exclusively

## Usage

``` r
private_odorant(
  receptor,
  sensillum = FALSE,
  response_matrix = door_default_values("door_response_matrix"),
  door_mappings = door_default_values("door_mappings"),
  zero = door_default_values("zero"),
  nshow = 5,
  tag
)
```

## Arguments

- receptor:

  character, name of a DoOR responding unit (one of `ORs$Or`)

- sensillum:

  logical, restrict the search to the sensillum the receptor is
  expressed in?

- response_matrix:

  DoOR response matrix, the input data to perform the search on

- door_mappings:

  the data frame containing the mapping information

- zero:

  character, an odorant that should be set to 0

- nshow:

  numeric, the number of private odorants to return

- tag:

  character, the chemical identifier to give the odorant names in (on of
  `colnames(odor)`)

## Value

a data.frame containing odorants and the response in the receptor of
interest as well as the maximum response of the remaining receptors and
their difference

## Examples

``` r
# load data
library(DoOR.data)

# find a private odorant for Gr21a.Gr63a (the carbon dioxide receptor)
# private_odorant("Gr21a.Gr63a", tag = "Name")

# now find an odorant that within the ab3 sensillum specifically activates
# Or22a
private_odorant("Or22a", tag = "Name", sensillum = TRUE)
#> 
#> >> Checking only against the ab3 sensillum (Or22a, Or22b, Or85b) <<
#>                             Or22a max.others n difference
#> ethyl hexanoate         0.7819367 0.23844314 1  0.5434936
#> ethyl 2-methylbutanoate 0.5368363 0.03107633 1  0.5057599
#> diethyl succinate       0.4659812 0.05652431 1  0.4094569
#> methyl octanoate        0.5249299 0.14747177 1  0.3774581
#> E2-hexenyl acetate      0.4271672 0.05042492 1  0.3767423
```
