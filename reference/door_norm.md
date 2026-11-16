# rescale the data values from 0 to 1

`door_norm` is used to normalize the data in values from 0 to 1.

## Usage

``` r
door_norm(x)
```

## Arguments

- x:

  a numeric vector

## Author

Shouwen Ma \<<shouwen.ma@uni-konstanz.de>\>

Daniel Münch \<<daniel.muench@uni-konstanz.de>\>

## Examples

``` r
# create example data
x <- rnorm(10)

# run door_norm on it
door_norm(x)
#>  [1] 0.2892677 0.7509271 0.0000000 0.6781686 0.8530656 1.0000000 0.1716402
#>  [8] 0.6107464 0.6116181 0.6008793
```
