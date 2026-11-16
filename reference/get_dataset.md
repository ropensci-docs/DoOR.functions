# getDataset

aggregates original data from a given study

## Usage

``` r
get_dataset(study, na.rm = FALSE)
```

## Arguments

- study:

  character, the name of the study you want to aggregate the dta from

- na.rm:

  logical, whether or not to exclude odorants that were not measured in
  the study

## Value

returns a data frame containing all the odorant responses measured in
`study`

## Author

Daniel Münch \<<daniel.muench@uni-konstanz.de>\>

## Examples

``` r
# load data
library(DoOR.data)
load_door_data(nointeraction = TRUE)

# get all recordings from the Hallem.2004.EN data set
get_dataset("Hallem.2004.EN", na.rm = TRUE)
#>        Class                    Name                    InChIKey     CID
#> 1       <NA>                     sfr                         SFR     SFR
#> 4      amine              putrescine KIDHWZJUCRJVML-UHFFFAOYSA-N    1045
#> 12    O ring       gamma-hexalactone JBFHTYHTHYHCDJ-UHFFFAOYSA-N   12756
#> 31    sulfid 3-methylthio-1-propanol CZUGFKJYCPYHHV-UHFFFAOYSA-N   10448
#> 34    sulfid            propanethiol SUVIGLJNEAMWEG-UHFFFAOYSA-N    7848
#> 36   terpene            alpha-pinene GRWFGVWFFZKLTI-UHFFFAOYSA-N    6654
#> 44   terpene         geranyl acetate HIGQPQRQIQDZMP-DHZHZOJOSA-N 1549026
#> 46   terpene                geraniol GLZPCOQZEFWAFX-JXMROGBWSA-N  637566
#> 48   terpene                linalool CDOSHBSSFJOMGT-UHFFFAOYSA-N    6549
#> 55   terpene                  citral WTEVQBCEXWBHNA-JXMROGBWSA-N  638011
#> 74  aldehyde              E2-hexenal MBDOYVRWFFCFHM-SNAWJCMRSA-N 5281168
#> 75    O ring                furfural HYBBIBNJHNGZAN-UHFFFAOYSA-N    7362
#> 77  aldehyde                 octanal NUJGJRNETVAIRJ-UHFFFAOYSA-N     454
#> 83    ketone                 acetone CSCPPACGZOOCGX-UHFFFAOYSA-N     180
#> 85    ketone             2-pentanone XNLICIUVMPYHGG-UHFFFAOYSA-N    7895
#> 86    ketone             2-heptanone CATSNJVOTSVZJV-UHFFFAOYSA-N    8051
#> 88    ketone         2,3-butanedione QSJXEFYPDANLFS-UHFFFAOYSA-N     650
#> 89    ketone    3-hydroxy-2-butanone ROWKJAVDOGWPAT-UHFFFAOYSA-N     179
#> 93    ketone           cyclohexanone JHIVVAPYMSGYDF-UHFFFAOYSA-N    7967
#> 94    ketone              2-octanone ZPVFWPFBNIEHGJ-UHFFFAOYSA-N    8093
#> 98      arom          benzyl alcohol WVDDGKGOMKODPV-UHFFFAOYSA-N     244
#> 99      arom       methyl salicylate OSWPMRLSEDHDFF-UHFFFAOYSA-N    4133
#> 103     arom            benzaldehyde HUMNYLRZRPPJDN-UHFFFAOYSA-N     240
#> 104     arom      phenylacetaldehyde DTUQWGWMVIHBKE-UHFFFAOYSA-N     998
#> 105     arom            acetophenone KWOLFJPFCHCOCG-UHFFFAOYSA-N    7410
#> 107     arom          2-methylphenol QWVGKYWNOKOFNN-UHFFFAOYSA-N     335
#> 120     arom          4-methylphenol IWDCLRJOBJJRNH-UHFFFAOYSA-N    2879
#> 121     arom           4-ethylphenol HXDOZKJGKXYMEW-UHFFFAOYSA-N   31242
#> 126     arom          benzyl acetate QUKGYYKBILRGFE-UHFFFAOYSA-N    8785
#> 127     arom          4-propylphenol KLSLBUSXWBJMEC-UHFFFAOYSA-N   12580
#> 128     arom          3-methylphenol RLSSMJSEOOYNOY-UHFFFAOYSA-N     342
#> 135  alcohol               1-butanol LRHPLDYGYMQRHN-UHFFFAOYSA-N     263
#> 137  alcohol               1-hexanol ZSIAUFGUXNUGDI-UHFFFAOYSA-N    8103
#> 138  alcohol               1-octanol KBPLFHHGFOOTCA-UHFFFAOYSA-N     957
#> 144  alcohol            1-octen-3-ol VSMOENVRRABVKN-UHFFFAOYSA-N   18827
#> 145  alcohol              E2-hexenol ZCHHRLHTBGRGOT-SNAWJCMRSA-N 5318042
#> 150  alcohol          2,3-butanediol OWBTYPJTUOEWEK-UHFFFAOYSA-N     262
#> 151  alcohol            cyclohexanol HPXRVTGHNJAIIH-UHFFFAOYSA-N    7966
#> 155  alcohol               3-octanol NMRPBPVERJPACX-UHFFFAOYSA-N   11527
#> 156  alcohol               1-nonanol ZWRUINPWMLAQRD-UHFFFAOYSA-N    8914
#> 164    ester           ethyl acetate XEKOWRVHYACXOJ-UHFFFAOYSA-N    8857
#> 166    ester           butyl acetate DKPFZGUDAPQIHT-UHFFFAOYSA-N   31272
#> 167    ester          pentyl acetate PGMYKACGEOXYJE-UHFFFAOYSA-N   12348
#> 170    ester       isopentyl acetate MLFHJEHSLIIPHL-UHFFFAOYSA-N   31276
#> 171    ester      E2-hexenyl acetate HRHOWZHRCRZVCU-WAYWQWQTSA-N 2733294
#> 173    ester          ethyl butyrate OBNCKNCVKJNDBV-UHFFFAOYSA-N    7762
#> 175    ester ethyl 3-hydroxybutyrate OMSUIQOIVADKIM-UHFFFAOYSA-N   62572
#> 176    ester        ethyl propionate FKRCODPIKNYEAC-UHFFFAOYSA-N    7749
#> 179    ester         ethyl hexanoate SHZIWNPUGXLXDT-UHFFFAOYSA-N   31265
#> 192   N ring                  indole SIKJAQJRHWYJAI-UHFFFAOYSA-N     798
#> 199    ester ethyl 2-methylbutanoate HCRBXQFHJMCTLF-UHFFFAOYSA-N   24020
#> 201    ester        ethyl pentanoate ICMAFTSLXCXHRK-UHFFFAOYSA-N   10882
#> 221    other                     oil                     solvent solvent
#> 225    other          carbon dioxide CURLTUGMZLYLDI-UHFFFAOYSA-N     280
#> 227   N ring             pyrrolidine RWRDLPDLKQPQOW-UHFFFAOYSA-N   31268
#> 666     <NA>     (R)-(+)-citronellal NEHNMFOYXAPHSD-SNVBAGLBSA-N   75427
#>           CAS   Or2a    Or7a    Or9a   Or10a   Or19a   Or22a  Or23a   Or33b
#> 1         SFR     NA  15.592      NA      NA      NA   6.186     NA   0.000
#> 4    110-60-1     NA      NA      NA      NA      NA      NA     NA      NA
#> 12   695-06-7     NA      NA      NA      NA      NA      NA 24.167      NA
#> 31   505-10-2     NA      NA      NA      NA      NA      NA     NA      NA
#> 34   107-03-9     NA      NA      NA      NA      NA      NA     NA      NA
#> 36    80-56-8     NA      NA      NA      NA      NA      NA     NA      NA
#> 44   105-87-3 16.667  44.833  29.167  19.333  54.167  27.333 17.167  -1.583
#> 46   106-24-1     NA      NA      NA      NA      NA      NA     NA      NA
#> 48    78-70-6     NA      NA      NA      NA      NA      NA     NA      NA
#> 55  5392-40-5     NA      NA      NA      NA      NA      NA     NA      NA
#> 74  6728-26-3 21.167 229.500  46.667  11.667  39.333  28.000 63.333  -6.083
#> 75    98-01-1 35.167      NA      NA      NA      NA      NA 24.333      NA
#> 77   124-13-0     NA      NA      NA      NA      NA      NA     NA      NA
#> 83    67-64-1     NA      NA      NA      NA      NA      NA     NA      NA
#> 85   107-87-9     NA      NA      NA      NA      NA      NA     NA      NA
#> 86   110-43-0 52.333   0.667  98.833  10.500 153.833  82.500 54.167  -7.333
#> 88   431-03-8 21.333  53.167 152.500  31.500  52.167  80.833 32.000  -4.167
#> 89   513-86-0 65.000      NA 203.000      NA      NA      NA     NA      NA
#> 93   108-94-1 41.500      NA      NA      NA      NA      NA 53.500      NA
#> 94   111-13-7     NA      NA      NA      NA 192.000      NA     NA      NA
#> 98   100-51-6     NA      NA      NA      NA      NA      NA     NA      NA
#> 99   119-36-8 20.000  14.833  25.000 249.500  61.667  17.500 16.000  -8.083
#> 103  100-52-7     NA 206.333      NA  70.833      NA      NA     NA      NA
#> 104  122-78-1     NA      NA      NA      NA      NA      NA     NA      NA
#> 105   98-86-2     NA      NA      NA 204.833      NA      NA     NA      NA
#> 107   95-48-7     NA      NA      NA      NA      NA      NA     NA      NA
#> 120  106-44-5     NA      NA      NA      NA      NA      NA     NA      NA
#> 121  123-07-9     NA      NA      NA      NA      NA      NA     NA      NA
#> 126  140-11-4     NA      NA      NA      NA      NA      NA     NA      NA
#> 127  645-56-7     NA      NA      NA      NA      NA      NA     NA      NA
#> 128  108-39-4     NA      NA      NA      NA      NA      NA     NA      NA
#> 135   71-36-3     NA 205.167      NA      NA      NA      NA     NA      NA
#> 137  111-27-3 41.500 113.167  95.833   5.500 152.500  68.167 57.167 -11.417
#> 138  111-87-5     NA      NA      NA      NA 136.500      NA     NA      NA
#> 144 3391-86-4 35.667  30.667  50.667   2.000 171.333 108.333 33.333 -14.917
#> 145  928-95-0     NA      NA      NA      NA      NA      NA     NA      NA
#> 150  513-85-9     NA      NA 189.333      NA      NA      NA     NA      NA
#> 151  108-93-0 51.000      NA      NA      NA      NA      NA 42.833      NA
#> 155  589-98-0     NA      NA      NA      NA      NA      NA     NA      NA
#> 156  143-08-8     NA      NA      NA      NA      NA      NA     NA      NA
#> 164  141-78-6 17.833  35.833  71.833  24.000  61.000  59.667 17.000  -3.583
#> 166  123-86-4     NA      NA      NA      NA 125.500 124.833     NA -15.500
#> 167  628-63-7 59.500  10.500  87.833  11.500 150.167 156.500 45.500 -13.167
#> 170  123-92-2     NA   1.500      NA 116.333 162.833 144.167     NA      NA
#> 171 2497-18-9     NA      NA      NA      NA      NA      NA     NA      NA
#> 173  105-54-4 20.333  10.833 121.167  25.000  93.333 168.000 24.167   5.000
#> 175 5405-41-4     NA      NA      NA      NA      NA      NA     NA -17.417
#> 176  105-37-3     NA      NA  80.000      NA      NA 124.167     NA  36.917
#> 179  123-66-0     NA      NA      NA      NA      NA      NA     NA  -7.167
#> 192  120-72-9     NA      NA      NA      NA      NA      NA     NA      NA
#> 199 7452-79-1     NA      NA      NA      NA      NA      NA     NA      NA
#> 201  539-82-2     NA      NA      NA      NA      NA      NA     NA      NA
#> 221   solvent 16.333  27.667  11.333  17.000  16.000  10.000  8.833   0.500
#> 225  124-38-9 17.167  26.000   8.167  19.500  12.667   6.000 14.667   2.417
#> 227  123-75-1     NA      NA      NA      NA      NA      NA     NA      NA
#> 666  106-23-0     NA      NA      NA      NA      NA      NA     NA      NA
#>       Or35a   Or43a   Or43b   Or47a  Or47b   Or49b   Or59b  Or65a   Or67a
#> 1        NA      NA      NA      NA 73.076      NA   7.008     NA      NA
#> 4        NA      NA      NA      NA     NA      NA      NA     NA      NA
#> 12       NA      NA      NA      NA 40.743      NA      NA     NA      NA
#> 31       NA      NA      NA 231.167     NA      NA      NA     NA      NA
#> 34       NA      NA      NA      NA     NA      NA      NA     NA      NA
#> 36       NA      NA      NA      NA     NA      NA      NA     NA      NA
#> 44   21.667  27.500  21.000   6.333 56.243  10.167  25.921 19.833  29.500
#> 46       NA      NA      NA      NA     NA      NA      NA     NA      NA
#> 48       NA      NA      NA      NA     NA      NA  -2.079     NA      NA
#> 55       NA      NA      NA      NA     NA      NA      NA     NA      NA
#> 74  200.167  84.500 103.667  39.500 64.076   9.833  20.087 14.667  71.500
#> 75       NA      NA      NA      NA     NA      NA      NA     NA      NA
#> 77  176.000      NA      NA      NA     NA      NA      NA     NA      NA
#> 83       NA      NA      NA      NA     NA      NA  84.921     NA      NA
#> 85  100.333      NA      NA      NA     NA      NA      NA     NA      NA
#> 86  116.833  71.833  75.167 182.833 33.493  16.000  26.754 39.500 111.000
#> 88   69.000  46.667  75.667  37.167 49.826  24.667 119.504 35.000  42.667
#> 89       NA      NA      NA      NA     NA      NA      NA     NA      NA
#> 93       NA 127.000      NA      NA 64.493      NA      NA     NA      NA
#> 94       NA      NA      NA      NA     NA      NA      NA     NA      NA
#> 98       NA  83.167      NA      NA     NA      NA      NA 16.333      NA
#> 99   23.667  55.333  18.500   0.167 72.993  27.000   4.504  5.833  25.333
#> 103      NA  72.667      NA      NA     NA      NA      NA  9.833      NA
#> 104      NA  35.667      NA      NA     NA      NA      NA     NA      NA
#> 105      NA      NA      NA      NA     NA      NA      NA     NA      NA
#> 107      NA      NA      NA      NA     NA 175.833      NA     NA      NA
#> 120      NA      NA      NA      NA     NA  67.500      NA     NA      NA
#> 121      NA      NA      NA      NA     NA  51.167      NA     NA      NA
#> 126      NA      NA      NA      NA     NA      NA      NA 25.667      NA
#> 127      NA      NA      NA      NA     NA  33.833      NA     NA      NA
#> 128      NA      NA      NA      NA     NA 102.333      NA     NA      NA
#> 135 222.000      NA      NA      NA     NA      NA      NA     NA      NA
#> 137 216.000 149.500 125.333  60.833  8.410  20.667  30.087 24.167  92.000
#> 138      NA  23.667      NA      NA     NA      NA      NA     NA      NA
#> 144 209.667 112.667  54.167  84.667 25.743  13.333  16.004 21.000  98.333
#> 145      NA      NA      NA      NA     NA      NA      NA     NA      NA
#> 150      NA      NA      NA      NA     NA      NA      NA     NA      NA
#> 151      NA 139.000      NA      NA 38.743      NA      NA     NA      NA
#> 155      NA      NA      NA      NA     NA      NA      NA     NA 110.167
#> 156 163.667      NA      NA      NA     NA      NA      NA     NA      NA
#> 164  33.333  30.333 178.167 115.000 52.826  17.833 121.087 17.833  42.667
#> 166      NA      NA 202.667      NA     NA      NA      NA     NA      NA
#> 167 201.500  52.667 112.833 255.833 26.160  15.000  36.421 36.167 130.000
#> 170      NA      NA      NA      NA     NA      NA      NA     NA 122.000
#> 171      NA      NA      NA      NA     NA      NA      NA     NA  46.333
#> 173 101.167  62.833 210.667  84.000 41.576   9.333  26.421 16.333 101.000
#> 175 185.500      NA      NA      NA     NA      NA      NA     NA      NA
#> 176      NA      NA      NA      NA     NA      NA  66.171     NA  55.667
#> 179      NA      NA  49.500      NA     NA      NA      NA     NA 154.833
#> 192      NA      NA      NA      NA     NA      NA      NA  7.167      NA
#> 199      NA      NA      NA      NA     NA      NA      NA     NA      NA
#> 201      NA      NA 164.667      NA     NA      NA      NA     NA      NA
#> 221  26.833  25.167   7.667  13.333 72.576   7.333  10.921 13.167  15.833
#> 225  20.000  23.500   6.333  15.333 71.826   7.833  10.587 17.333  18.500
#> 227      NA      NA      NA      NA     NA      NA      NA 59.167      NA
#> 666      NA      NA      NA      NA     NA      NA      NA     NA      NA
#>       Or67c   Or82a   Or85a   Or85b  Or85f   Or88a   Or98a
#> 1        NA      NA      NA      NA     NA   0.000      NA
#> 4        NA      NA      NA  79.500     NA      NA      NA
#> 12       NA      NA      NA      NA 59.000      NA      NA
#> 31       NA      NA      NA      NA     NA      NA      NA
#> 34       NA      NA      NA 116.667     NA      NA      NA
#> 36       NA  19.500      NA      NA     NA      NA      NA
#> 44    5.000 211.667  10.833  64.333  8.000   1.333  81.167
#> 46       NA  30.333      NA      NA     NA      NA      NA
#> 48       NA  34.545      NA      NA     NA      NA 159.333
#> 55       NA  71.667      NA      NA     NA      NA      NA
#> 74   58.833  12.333  30.500 186.500 35.333  -5.083  45.833
#> 75       NA      NA      NA      NA 56.333      NA      NA
#> 77       NA      NA      NA      NA     NA      NA      NA
#> 83       NA      NA      NA      NA     NA      NA      NA
#> 85       NA      NA      NA      NA     NA      NA      NA
#> 86   53.000  40.000  42.833 238.667 54.000  -8.583 220.833
#> 88   47.667  34.500  36.667 175.833 31.500   5.583  44.667
#> 89       NA      NA      NA      NA     NA      NA      NA
#> 93       NA      NA      NA      NA     NA      NA      NA
#> 94       NA      NA      NA      NA     NA      NA      NA
#> 98       NA      NA      NA      NA     NA      NA      NA
#> 99    2.333  12.333   6.333  52.167 19.333  -6.500  29.500
#> 103      NA      NA      NA      NA 41.667      NA      NA
#> 104      NA      NA      NA      NA     NA      NA      NA
#> 105      NA      NA      NA      NA     NA      NA      NA
#> 107      NA      NA      NA      NA     NA      NA      NA
#> 120      NA      NA      NA      NA     NA      NA      NA
#> 121      NA      NA      NA      NA     NA      NA      NA
#> 126      NA      NA      NA      NA     NA      NA      NA
#> 127      NA      NA      NA      NA     NA      NA      NA
#> 128      NA      NA      NA      NA     NA      NA      NA
#> 135      NA      NA      NA      NA     NA      NA      NA
#> 137  99.167  47.000 141.667 247.000 64.000 -10.583 167.833
#> 138      NA      NA      NA      NA     NA      NA      NA
#> 144  25.167  35.333  45.000 234.167 32.667 -11.750 196.833
#> 145 100.333      NA 141.500      NA     NA      NA 191.667
#> 150      NA      NA      NA      NA     NA      NA      NA
#> 151      NA      NA      NA      NA 62.167      NA      NA
#> 155      NA      NA      NA 245.000     NA      NA      NA
#> 156      NA      NA      NA      NA     NA      NA      NA
#> 164  35.167  27.167  56.833  39.333 25.333  -0.500  27.000
#> 166      NA      NA      NA      NA     NA      NA      NA
#> 167  28.167  38.833  34.333 254.667 38.333 -11.917 231.333
#> 170      NA      NA      NA      NA     NA      NA      NA
#> 171  10.667      NA      NA      NA     NA      NA      NA
#> 173 135.000  33.500 132.167 141.833 30.333  -4.417 113.167
#> 175  54.333      NA      NA      NA     NA      NA      NA
#> 176  47.000      NA      NA      NA     NA      NA  41.833
#> 179      NA      NA      NA      NA     NA      NA      NA
#> 192      NA      NA      NA      NA     NA  -5.083      NA
#> 199  91.000      NA  58.167      NA     NA      NA      NA
#> 201      NA      NA      NA      NA     NA      NA      NA
#> 221   4.333  13.667  11.000  58.333  4.000   1.250  21.167
#> 225   6.833  13.833  15.000  44.000  4.667  -0.667  45.667
#> 227      NA      NA      NA      NA     NA  81.333      NA
#> 666      NA  49.333      NA      NA     NA      NA      NA
```
