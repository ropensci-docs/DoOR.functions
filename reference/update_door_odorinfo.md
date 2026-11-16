# update_door_odorinfo

Update the DoOR odor data with info from `odor`. For the function to
work, all DoOR data has to be loaded to the current environment.

## Usage

``` r
update_door_odorinfo()
```

## Author

Daniel Münch, <daniel@muench.bio>

## Examples

``` r
# load data
load_door_data(nointeraction = TRUE)  
# modify odor
odor[1,1] <- "acid"

# run 
update_door_odorinfo()

# check that data sets have been updated
head(Or22a)
#>   Class               Name                    InChIKey   CID       CAS
#> 1  <NA>                sfr                         SFR   SFR       SFR
#> 2 other              water XLYOFNOQVPJJNP-UHFFFAOYSA-N   962 7732-18-5
#> 3 amine ammonium hydroxide VHUUQVKOLVNVRT-UHFFFAOYSA-N 14923 1336-21-6
#> 4 amine         putrescine KIDHWZJUCRJVML-UHFFFAOYSA-N  1045  110-60-1
#> 5 amine         cadaverine VHRGRCVQAFMJIZ-UHFFFAOYSA-N   273  462-94-2
#> 6 amine            ammonia QGZKDVFQNNGYKY-UHFFFAOYSA-N   222 7664-41-7
#>   Hallem.2006.EN Dobritsa.2003.EN Stensmyr.2003.WT Schmuker.2007.TR
#> 1              4               NA               NA                4
#> 2             NA               NA               NA               NA
#> 3             17               NA               NA               NA
#> 4             16               NA               NA                3
#> 5             17               NA               NA               NA
#> 6             NA               NA               NA                3
#>   Pelz.2006.ALEC50 Pelz.2006.AntEC50 Pelz.2005.ALnmr Pelz.2005.Antnmr
#> 1               NA                NA               0                0
#> 2               NA                NA              NA               NA
#> 3               NA                NA              NA               NA
#> 4               NA                NA              NA               NA
#> 5               NA                NA              NA               NA
#> 6               NA                NA              NA               NA
#>   Gabler.2013.AL Bruyne.2001.WT Bruyne.2010.WT Marshall.2010.WT Hallem.2004.EN
#> 1              0              4              0            0.000          6.186
#> 2             NA             NA             NA           60.571             NA
#> 3             NA             NA             NA           44.286             NA
#> 4             NA             NA             NA           28.000             NA
#> 5             NA             NA             NA               NA             NA
#> 6             NA             NA             NA               NA             NA
#>   Hallem.2004.WT
#> 1          6.915
#> 2             NA
#> 3             NA
#> 4             NA
#> 5             NA
#> 6             NA

```
