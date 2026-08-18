# map_receptor

Identifying the source of unknown response data by correlating it agains
all DoOR responding units.

Identifying the source of unknown response data by correlating it agains
all DoOR responding units.

## Usage

``` r
map_receptor(
  data,
  response_matrix = door_default_values("door_response_matrix"),
  sub,
  threshold.p,
  threshold.cor,
  nshow
)

map_receptor(
  data,
  response_matrix = door_default_values("door_response_matrix"),
  sub,
  threshold.p,
  threshold.cor,
  nshow
)
```

## Arguments

- data:

  data frame, containing two columns, one called "odorants" and one
  "responses" providing InChIKeys and odorant responses respectively.

- response_matrix:

  output is a numeric vector that contains the Pearson Correlation
  Coefficient between given data and selected consensus data in

- sub:

  character, a subset of responding units returned response matrix

- threshold.p:

  numeric, a p-value threshold, only correlations below will be returned

- threshold.cor:

  numeric, a correlation-coefficient threshold, only correlations above
  will be returned

- nshow:

  numeric, if defined, only this number of results will be

## Author

Shouwen Ma \<<shouwen.ma@uni-konstanz.de>\>

Daniel Münch \<<daniel.muench@uni-konstanz.de>\>

## Examples

``` r
# load data
load_door_data(nointeraction = TRUE)

# pick example data
data <- data.frame(odorants  = Or22a$InChIKey,
                   responses = Or22a$Hallem.2004.EN)
data <- na.omit(data)

# find the corresponding receptor / responding unit
map_receptor(data = data)
#> skipped Or22c, Or24a, Or67d, pb2A as overlap (n) was < 3
#>             responding.unit  n         cor      p.value
#> Or22a                 Or22a 16  0.97330896 2.411584e-10
#> Or59c                 Or59c  9  0.88242782 1.632627e-03
#> Or9a                   Or9a 16  0.85276703 2.700050e-05
#> Or43b                 Or43b 16  0.79518371 2.313586e-04
#> Or67a                 Or67a 16  0.79176325 2.572690e-04
#> Or47a                 Or47a 16  0.72804758 1.385630e-03
#> Or2a                   Or2a 16  0.70479672 2.297156e-03
#> Or33c                 Or33c  6  0.69696356 1.238325e-01
#> Or98a                 Or98a 16  0.67425019 4.176814e-03
#> Or49a                 Or49a 14  0.66615361 9.291311e-03
#> ac1BC                 ac1BC  6  0.65659482 1.566423e-01
#> Or94b                 Or94b 14  0.63649625 1.438747e-02
#> Or19a                 Or19a 16  0.63081664 8.790115e-03
#> Or85c                 Or85c 14  0.60963985 2.063069e-02
#> Or85f                 Or85f 16  0.56826475 2.163953e-02
#> Or65a                 Or65a 16  0.55632710 2.522050e-02
#> ab5B                   ab5B 15  0.54060183 3.746370e-02
#> Or59a                 Or59a 14  0.52776838 5.241598e-02
#> Ir75d                 Ir75d  5  0.52095007 3.680658e-01
#> Or85b                 Or85b 16  0.50924681 4.392992e-02
#> Or67c                 Or67c 16  0.49794238 4.966312e-02
#> Or45a                 Or45a 14  0.49760175 7.020797e-02
#> Or85d                 Or85d  9  0.48592684 1.847643e-01
#> ab4B                   ab4B 16  0.47611524 6.228175e-02
#> Or42b                 Or42b 16  0.47398484 6.362844e-02
#> ac1B                   ac1B  8  0.46318881 2.477438e-01
#> Or22b                 Or22b 11  0.44930742 1.656274e-01
#> Or85e                 Or85e  6  0.43414674 3.896946e-01
#> ab2B                   ab2B 16  0.42262954 1.029175e-01
#> ac1                     ac1 16  0.41993818 1.053615e-01
#> Or42a                 Or42a 14  0.39804599 1.586720e-01
#> Ir64a.DC4         Ir64a.DC4  5  0.39612935 5.091526e-01
#> Or49b                 Or49b 16  0.38344243 1.426251e-01
#> Or45b                 Or45b 14  0.37128448 1.912066e-01
#> ac3B                   ac3B 14  0.36544411 1.988322e-01
#> Or85a                 Or85a 16  0.35467189 1.776836e-01
#> Or1a                   Or1a 14  0.34649440 2.248872e-01
#> Or35a                 Or35a 16  0.31753759 2.307431e-01
#> Or23a                 Or23a 16  0.30793288 2.459328e-01
#> Or13a                 Or13a 16  0.30089844 2.574429e-01
#> ac1A                   ac1A 11  0.29914593 3.715140e-01
#> Ir64a.DP1m       Ir64a.DP1m  5  0.24681292 6.889684e-01
#> Or43a                 Or43a 16  0.21957875 4.138642e-01
#> Or59b                 Or59b 16  0.20742642 4.407997e-01
#> Or33b                 Or33b 16  0.20172016 4.537477e-01
#> Or67b                 Or67b 15  0.19222954 4.924876e-01
#> Or33a                 Or33a 14  0.14653356 6.171644e-01
#> Or94a                 Or94a 14  0.11379043 6.985109e-01
#> Or92a                 Or92a 16  0.10564944 6.969726e-01
#> Or74a                 Or74a 14  0.09066206 7.579042e-01
#> ac2A                   ac2A 11  0.06892160 8.404222e-01
#> Ir75a                 Ir75a  5  0.06720159 9.145007e-01
#> Or69a                 Or69a  8  0.04747053 9.111264e-01
#> Or10a                 Or10a 16  0.01137190 9.666592e-01
#> ac2                     ac2 16 -0.00299004 9.912315e-01
#> ac3A                   ac3A 12 -0.07111781 8.261584e-01
#> ac3_noOr35a     ac3_noOr35a 16 -0.07129613 7.930252e-01
#> Or30a                 Or30a 14 -0.07501165 7.988326e-01
#> Ir92a                 Ir92a  5 -0.07827535 9.004386e-01
#> Or82a                 Or82a 16 -0.15964051 5.548075e-01
#> Or71a                 Or71a 12 -0.17163567 5.937722e-01
#> ac2B                   ac2B  8 -0.18689747 6.576423e-01
#> Or7a                   Or7a 16 -0.19461594 4.701299e-01
#> ac2BC                 ac2BC  6 -0.19862941 7.059742e-01
#> ac4                     ac4 16 -0.22286950 4.067226e-01
#> Gr21a.Gr63a     Gr21a.Gr63a 14 -0.23718054 4.142385e-01
#> Or83c                 Or83c 13 -0.23941804 4.308047e-01
#> Or88a                 Or88a 16 -0.32014767 2.267201e-01
#> Ir31a                 Ir31a  5 -0.32820037 5.897504e-01
#> Or46a                 Or46a  6 -0.62554327 1.840740e-01
#> Or47b                 Or47b 16 -0.70730528 2.180129e-03
#> Ir76a                 Ir76a  5 -0.74892420 1.452005e-01
#> Ir41a                 Ir41a  5 -0.78957881 1.121403e-01
#> Ir84a                 Ir84a  5 -0.92666215 2.357708e-02
# load data
load_door_data(nointeraction = TRUE)

# pick example data
data <- data.frame(odorants  = Or22a$InChIKey,
                   responses = Or22a$Hallem.2004.EN)
data <- na.omit(data)

# find the corresponding receptor / responding unit
map_receptor(data = data)
#> skipped Or22c, Or24a, Or67d, pb2A as overlap (n) was < 3
#>             responding.unit  n         cor      p.value
#> Or22a                 Or22a 16  0.97330896 2.411584e-10
#> Or59c                 Or59c  9  0.88242782 1.632627e-03
#> Or9a                   Or9a 16  0.85276703 2.700050e-05
#> Or43b                 Or43b 16  0.79518371 2.313586e-04
#> Or67a                 Or67a 16  0.79176325 2.572690e-04
#> Or47a                 Or47a 16  0.72804758 1.385630e-03
#> Or2a                   Or2a 16  0.70479672 2.297156e-03
#> Or33c                 Or33c  6  0.69696356 1.238325e-01
#> Or98a                 Or98a 16  0.67425019 4.176814e-03
#> Or49a                 Or49a 14  0.66615361 9.291311e-03
#> ac1BC                 ac1BC  6  0.65659482 1.566423e-01
#> Or94b                 Or94b 14  0.63649625 1.438747e-02
#> Or19a                 Or19a 16  0.63081664 8.790115e-03
#> Or85c                 Or85c 14  0.60963985 2.063069e-02
#> Or85f                 Or85f 16  0.56826475 2.163953e-02
#> Or65a                 Or65a 16  0.55632710 2.522050e-02
#> ab5B                   ab5B 15  0.54060183 3.746370e-02
#> Or59a                 Or59a 14  0.52776838 5.241598e-02
#> Ir75d                 Ir75d  5  0.52095007 3.680658e-01
#> Or85b                 Or85b 16  0.50924681 4.392992e-02
#> Or67c                 Or67c 16  0.49794238 4.966312e-02
#> Or45a                 Or45a 14  0.49760175 7.020797e-02
#> Or85d                 Or85d  9  0.48592684 1.847643e-01
#> ab4B                   ab4B 16  0.47611524 6.228175e-02
#> Or42b                 Or42b 16  0.47398484 6.362844e-02
#> ac1B                   ac1B  8  0.46318881 2.477438e-01
#> Or22b                 Or22b 11  0.44930742 1.656274e-01
#> Or85e                 Or85e  6  0.43414674 3.896946e-01
#> ab2B                   ab2B 16  0.42262954 1.029175e-01
#> ac1                     ac1 16  0.41993818 1.053615e-01
#> Or42a                 Or42a 14  0.39804599 1.586720e-01
#> Ir64a.DC4         Ir64a.DC4  5  0.39612935 5.091526e-01
#> Or49b                 Or49b 16  0.38344243 1.426251e-01
#> Or45b                 Or45b 14  0.37128448 1.912066e-01
#> ac3B                   ac3B 14  0.36544411 1.988322e-01
#> Or85a                 Or85a 16  0.35467189 1.776836e-01
#> Or1a                   Or1a 14  0.34649440 2.248872e-01
#> Or35a                 Or35a 16  0.31753759 2.307431e-01
#> Or23a                 Or23a 16  0.30793288 2.459328e-01
#> Or13a                 Or13a 16  0.30089844 2.574429e-01
#> ac1A                   ac1A 11  0.29914593 3.715140e-01
#> Ir64a.DP1m       Ir64a.DP1m  5  0.24681292 6.889684e-01
#> Or43a                 Or43a 16  0.21957875 4.138642e-01
#> Or59b                 Or59b 16  0.20742642 4.407997e-01
#> Or33b                 Or33b 16  0.20172016 4.537477e-01
#> Or67b                 Or67b 15  0.19222954 4.924876e-01
#> Or33a                 Or33a 14  0.14653356 6.171644e-01
#> Or94a                 Or94a 14  0.11379043 6.985109e-01
#> Or92a                 Or92a 16  0.10564944 6.969726e-01
#> Or74a                 Or74a 14  0.09066206 7.579042e-01
#> ac2A                   ac2A 11  0.06892160 8.404222e-01
#> Ir75a                 Ir75a  5  0.06720159 9.145007e-01
#> Or69a                 Or69a  8  0.04747053 9.111264e-01
#> Or10a                 Or10a 16  0.01137190 9.666592e-01
#> ac2                     ac2 16 -0.00299004 9.912315e-01
#> ac3A                   ac3A 12 -0.07111781 8.261584e-01
#> ac3_noOr35a     ac3_noOr35a 16 -0.07129613 7.930252e-01
#> Or30a                 Or30a 14 -0.07501165 7.988326e-01
#> Ir92a                 Ir92a  5 -0.07827535 9.004386e-01
#> Or82a                 Or82a 16 -0.15964051 5.548075e-01
#> Or71a                 Or71a 12 -0.17163567 5.937722e-01
#> ac2B                   ac2B  8 -0.18689747 6.576423e-01
#> Or7a                   Or7a 16 -0.19461594 4.701299e-01
#> ac2BC                 ac2BC  6 -0.19862941 7.059742e-01
#> ac4                     ac4 16 -0.22286950 4.067226e-01
#> Gr21a.Gr63a     Gr21a.Gr63a 14 -0.23718054 4.142385e-01
#> Or83c                 Or83c 13 -0.23941804 4.308047e-01
#> Or88a                 Or88a 16 -0.32014767 2.267201e-01
#> Ir31a                 Ir31a  5 -0.32820037 5.897504e-01
#> Or46a                 Or46a  6 -0.62554327 1.840740e-01
#> Or47b                 Or47b 16 -0.70730528 2.180129e-03
#> Ir76a                 Ir76a  5 -0.74892420 1.452005e-01
#> Ir41a                 Ir41a  5 -0.78957881 1.121403e-01
#> Ir84a                 Ir84a  5 -0.92666215 2.357708e-02
```
