# Calculate the sparseness of a vector.

Sparseness can be calculated as lifetime kurtosis (LTK, Willmore and
Tolhurst, 2001) or as lifetime sparseness (LTS, Bhandawat et al., 2007).

## Usage

``` r
sparse(x, method = "ltk")
```

## Arguments

- x:

  numerical input vector

- method:

  type of sparseness measure, either 'ltk' for lifetime kurtosis or
  'lts' for lifetime sparseness (see references).

## Details

LTS scales between \\0,1\\ while LTK is not restricted. LTS only takes
positive values.

## References

Bhandawat, V., Olsen, S.R., Gouwens, N.W., Schlief, M.L., Wilson, R.I.,
2007. Sensory processing in the Drosophila antennal lobe increases
reliability and separability of ensemble odor representations. Nature
neuroscience 10, 1474–82. doi:10.1038/nn1976

Willmore, B., Tolhurst, D.J., 2001. Characterizing the sparseness of
neural codes. Network 12, 255–270. doi:10.1080/net.12.3.255.270

## Author

Daniel Münch \<<daniel.muench@uni-konstanz.de>\>
