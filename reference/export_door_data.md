# export data

export odor response data and supported data

## Usage

``` r
export_door_data(directory, sep = ";", ...)
```

## Arguments

- directory:

  character string, output dir

- sep:

  separator used in write.csv

- ...:

  more parameters passed to write.csv

## Details

Please load ORs from data package DoOR.data by typing (`data(ORs)`)
before use.

## Author

Daniel Münch \<<daniel.muench@uni-giessen.de>\>

## Examples

``` r
if (FALSE) { # \dontrun{
# load data
library(DoOR.data)
library(DoOR.functions)
load_door_data()

# export odorant response data only
export_door_data(".")   
} # }
```
