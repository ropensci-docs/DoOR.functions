# Remove a study from DoOR

Use this function to remove a study from the DoOR database.
`import_new_data.R` uses this function when it detects an existing study
during the import process (e.g. because you imported updated data).

## Usage

``` r
remove_study(
  study,
  receptors = door_default_values("ORs"),
  responseRange = door_default_values("door_response_range"),
  weightGlobNorm = door_default_values("door_global_normalization_weights")
)
```

## Arguments

- study:

  a string containing the name of the study you want to remove (e.g.
  'Bruyne.2001.WT')

- receptors:

  a vector of all the receptors to be checked. Defaults to all receptors
  exidting in DoOR.

- responseRange:

  the dataframe containing the info about the response ranges of all
  studies (`door_response_range`)

- weightGlobNorm:

  the dataframe containing the info about the relative weights between
  receptors (`door_global_normalization_weights`)

## See also

[`import_new_data`](https://docs.ropensci.org/DoOR.functions/reference/import_new_data.md)

## Author

Daniel Münch \<<daniel.muench@uni-konstanz.de>\>

## Examples

``` r
# load data
library(DoOR.data)
load_door_data(nointeraction = TRUE)

# remove Bruyne.2001.WT from DoOR
remove_study('Bruyne.2001.WT')
#> removed Bruyne.2001.WT from Or7a .
#> removed Bruyne.2001.WT from Or10a .
#> removed Bruyne.2001.WT from Or13a .
#> removed Bruyne.2001.WT from Or22a .
#> removed Bruyne.2001.WT from Or42b .
#> removed Bruyne.2001.WT from Or49b .
#> removed Bruyne.2001.WT from Or59b .
#> removed Bruyne.2001.WT from Or67c .
#> removed Bruyne.2001.WT from Or82a .
#> removed Bruyne.2001.WT from Or85b .
#> removed Bruyne.2001.WT from Or92a .
#> removed Bruyne.2001.WT from Or98a .
#> removed Bruyne.2001.WT from Gr21a.Gr63a .
#> removed Bruyne.2001.WT from ab2B .
#> removed Bruyne.2001.WT from ab4B .
#> removed Bruyne.2001.WT from ab5B .
#> removed Bruyne.2001.WT from 'door_response_range'
#> removed Bruyne.2001.WT from 'door_global_normalization_weights'
```
