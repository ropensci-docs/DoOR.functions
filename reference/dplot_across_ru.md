# dplot_across_ru

barplot of DoOR responses of a set of odorant across all responding
units in DoOR

## Usage

``` r
dplot_across_ru(
  odorant,
  response_matrix = door_default_values("door_response_matrix"),
  odor_data = door_default_values("odor"),
  zero = door_default_values("zero"),
  tag = "Name",
  limits,
  base_size = 12
)
```

## Arguments

- odorant:

  character vecto, one or several InChIKeys

- response_matrix:

  DoOR response matrix, a DoOR response matrix as data source

- odor_data:

  data frame, contains the odorant information.

- zero:

  character, an InChIKey of the odorant that should be set to 0

- tag:

  character, the chemical identifier to plot as odorant name (one of
  colnames(odor))

- limits:

  numeric of length 2, if provided the ylim will range accordingly

- base_size:

  numeric, the base font size for the ggplot2 plot

## Value

a ggplot object

## Author

Daniel Münch \<<daniel.muench@uni-konstanz.de>\>

## Examples

``` r
# load data
library(DoOR.data)
library(DoOR.functions)
data(odor)

# plot activation pattern of one or several odorants
dplot_across_ru(trans_id("123-92-2"), tag = "CAS")

dplot_across_ru(odor$InChIKey[4:10])

```
