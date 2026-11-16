# load2list

returns all original DoOR response data as a list

## Usage

``` r
load2list()
```

## Value

a list

## Author

Daniel Münch \<<daniel.muench@uni-konstanz.de>\>

## Examples

``` r
# load DoOR.data
library(DoOR.data)
load_door_data(nointeraction = TRUE)

# write the data into a list
lst <- load2list()
```
