# default values for DoOR functions

`door_default_values` is used to return default values for DoOR
functions.

## Usage

``` r
door_default_values(DoOR_default)
```

## Arguments

- DoOR_default:

  a character string, indicating which argument is to be returned for
  DoOR functions.

## Details

There are six categories for default value. real number, integer,
logical, NULL, character string and character vector.

## Author

Shouwen Ma \<<shouwen.ma@uni-konstanz.de>\>

## Examples

``` r
# extract DoOR default values
door_default_values(DoOR_default = "select.MD")
#> [1] TRUE
```
