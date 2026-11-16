# reset SFR

A function for reseting SFR to zero

## Usage

``` r
reset_sfr(x, sfr)
```

## Arguments

- x:

  numeric or DoOR response matrix, input values

- sfr:

  numeric or character, either a value to subtract if x is a vector or
  an InChIKey if x is a DoOR response matrix

## Details

Performs a simple subtraction of the SFR value.

## Author

Daniel Münch \<<daniel.muench@uni-konstanz.de>\>

## Examples

``` r
# load data
library(DoOR.data)
data(door_response_matrix)

# create a response matrix with the SFR reset to 0
door_response_matrix_SFRreset <- reset_sfr(door_response_matrix, "SFR")
```
