# count_studies

returns a matrix indiating how many studies have recorded individual
receptor-odorant combinations

## Usage

``` r
count_studies(
  ors = door_default_values("ORs"),
  odor_data = door_default_values("odor"),
  char.columns = door_default_values("num.charColumns"),
  ident = door_default_values("ident")
)
```

## Arguments

- ors:

  data.frame containing all receptors exidting in DoOR.

- odor_data:

  data.frame containing information about the odorants in DoOR.

- char.columns:

  number of character columns in each receptor data.frame.

- ident:

  odorant identifier to be used as rownames.

## Value

matrix

## Examples

``` r
# load some data
library(DoOR.data)
load_door_data(nointeraction = TRUE)

#run count studies and plot the result
count <- count_studies()
image(count)

head(count)
#>                             ac1A ac1B ac2A ac2B ac3A ac3B ac4 Or1a Or2a Or7a
#> SFR                            2    1    2    1    3    3   3    1    3   10
#> XLYOFNOQVPJJNP-UHFFFAOYSA-N    1    0    1    0    2    2   2    1    1    2
#> VHUUQVKOLVNVRT-UHFFFAOYSA-N    1    0    1    0    2    2   2    0    1    2
#> KIDHWZJUCRJVML-UHFFFAOYSA-N    2    1    2    1    3    3   3    0    1    4
#> VHRGRCVQAFMJIZ-UHFFFAOYSA-N    0    0    0    0    1    1   1    0    1    2
#> QGZKDVFQNNGYKY-UHFFFAOYSA-N    1    1    1    1    1    1   1    0    0    2
#>                             Or9a Or10a Or13a Or19a Or22a Or22b Or22c Or23a
#> SFR                            2     6     7     3    10     0     2     1
#> XLYOFNOQVPJJNP-UHFFFAOYSA-N    1     1     2     0     1     0     1     0
#> VHUUQVKOLVNVRT-UHFFFAOYSA-N    2     2     1     2     2     0     0     1
#> KIDHWZJUCRJVML-UHFFFAOYSA-N    2     3     2     2     3     0     0     1
#> VHRGRCVQAFMJIZ-UHFFFAOYSA-N    1     1     0     2     1     0     0     1
#> QGZKDVFQNNGYKY-UHFFFAOYSA-N    0     1     1     0     1     0     0     0
#>                             Or24a Or30a Or33a Or33b Or33c Or35a Or42a Or42b
#> SFR                             2     3     1     4     1     3     6     7
#> XLYOFNOQVPJJNP-UHFFFAOYSA-N     1     2     1     1     0     1     3     2
#> VHUUQVKOLVNVRT-UHFFFAOYSA-N     0     0     0     1     0     1     1     1
#> KIDHWZJUCRJVML-UHFFFAOYSA-N     0     0     0     1     0     1     1     2
#> VHRGRCVQAFMJIZ-UHFFFAOYSA-N     0     0     0     1     0     1     0     0
#> QGZKDVFQNNGYKY-UHFFFAOYSA-N     0     0     0     0     0     0     0     1
#>                             Or43a Or43b Or45a Or45b Or46a Or47a Or47b Or49a
#> SFR                             1     3     3     3     3     4     6     3
#> XLYOFNOQVPJJNP-UHFFFAOYSA-N     0     1     2     2     1     1     0     2
#> VHUUQVKOLVNVRT-UHFFFAOYSA-N     1     2     0     0     1     1     1     0
#> KIDHWZJUCRJVML-UHFFFAOYSA-N     1     2     0     0     1     1     1     0
#> VHRGRCVQAFMJIZ-UHFFFAOYSA-N     1     1     0     0     0     1     1     0
#> QGZKDVFQNNGYKY-UHFFFAOYSA-N     0     0     0     0     0     0     0     0
#>                             Or49b Or59a Or59b Or59c Or65a Or67a Or67b Or67c
#> SFR                             3     3     8     4     2     2     4     3
#> XLYOFNOQVPJJNP-UHFFFAOYSA-N     1     1     1     1     0     0     2     1
#> VHUUQVKOLVNVRT-UHFFFAOYSA-N     2     0     2     1     1     1     0     2
#> KIDHWZJUCRJVML-UHFFFAOYSA-N     3     0     3     1     1     1     0     3
#> VHRGRCVQAFMJIZ-UHFFFAOYSA-N     1     0     1     0     1     1     0     1
#> QGZKDVFQNNGYKY-UHFFFAOYSA-N     1     0     1     0     0     0     0     1
#>                             Or67d Or71a Or74a Or82a Or85a Or85b Or85c Or85d
#> SFR                             2     4     3     6     1     4     3     3
#> XLYOFNOQVPJJNP-UHFFFAOYSA-N     0     1     2     2     0     1     2     1
#> VHUUQVKOLVNVRT-UHFFFAOYSA-N     0     1     0     2     1     1     0     1
#> KIDHWZJUCRJVML-UHFFFAOYSA-N     0     1     0     3     1     5     0     1
#> VHRGRCVQAFMJIZ-UHFFFAOYSA-N     0     0     0     1     1     1     0     0
#> QGZKDVFQNNGYKY-UHFFFAOYSA-N     0     0     0     1     0     1     0     0
#>                             Or85e Or85f Or88a Or92a Or94a Or94b Or98a
#> SFR                             1     1     3     4     4     4     3
#> XLYOFNOQVPJJNP-UHFFFAOYSA-N     0     0     0     1     2     2     1
#> VHUUQVKOLVNVRT-UHFFFAOYSA-N     0     1     1     1     0     0     2
#> KIDHWZJUCRJVML-UHFFFAOYSA-N     0     1     1     2     0     0     3
#> VHRGRCVQAFMJIZ-UHFFFAOYSA-N     0     1     1     0     0     0     1
#> QGZKDVFQNNGYKY-UHFFFAOYSA-N     0     0     0     1     0     0     1
#>                             Gr21a.Gr63a ab2B ab4B ab5B pb2A Or69a ac1 ac2
#> SFR                                   5    4    4    3    3     1   1   1
#> XLYOFNOQVPJJNP-UHFFFAOYSA-N           0    1    1    1    1     0   1   1
#> VHUUQVKOLVNVRT-UHFFFAOYSA-N           0    1    1    1    1     0   1   1
#> KIDHWZJUCRJVML-UHFFFAOYSA-N           0    2    2    2    1     0   1   1
#> VHRGRCVQAFMJIZ-UHFFFAOYSA-N           0    0    1    0    0     0   1   1
#> QGZKDVFQNNGYKY-UHFFFAOYSA-N           3    1    2    1    0     0   0   0
#>                             ac3_noOr35a Ir31a Ir41a Ir75a Ir75d Ir76a Ir84a
#> SFR                                   1     1     1     2     1     1     2
#> XLYOFNOQVPJJNP-UHFFFAOYSA-N           1     1     1     2     1     1     2
#> VHUUQVKOLVNVRT-UHFFFAOYSA-N           1     1     1     2     1     1     2
#> KIDHWZJUCRJVML-UHFFFAOYSA-N           1     1     1     2     1     1     2
#> VHRGRCVQAFMJIZ-UHFFFAOYSA-N           1     1     1     2     1     1     2
#> QGZKDVFQNNGYKY-UHFFFAOYSA-N           0     0     0     0     0     0     0
#>                             Ir92a Ir64a.DC4 Ir64a.DP1m ac1BC ac2BC Or83c
#> SFR                             1         1          1     1     1     1
#> XLYOFNOQVPJJNP-UHFFFAOYSA-N     1         1          1     1     1     0
#> VHUUQVKOLVNVRT-UHFFFAOYSA-N     1         1          1     1     1     0
#> KIDHWZJUCRJVML-UHFFFAOYSA-N     1         1          1     1     1     0
#> VHRGRCVQAFMJIZ-UHFFFAOYSA-N     1         1          1     0     0     0
#> QGZKDVFQNNGYKY-UHFFFAOYSA-N     0         0          0     0     0     1
```
