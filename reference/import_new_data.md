# Import new data into DoOR

Import or update new data and update
`door_global_normalization_weights`, `door_response_range`, `odor`,
`ORs` and receptor data frames.

## Usage

``` r
import_new_data(
  file.name,
  dataFormat = door_default_values("door_data_format"),
  odor_data = door_default_values("odor"),
  weightGlobNorm = door_default_values("door_global_normalization_weights"),
  responseRange = door_default_values("door_response_range"),
  receptors = door_default_values("ORs"),
  ident = door_default_values("ident"),
  round = 3
)
```

## Arguments

- file.name:

  character string, the name of given file that contains response values
  of one or more odorant receptors, either a .csv or .txt file.

- dataFormat:

  data frame, a data frame does not contain any response value but
  odorant information.

- odor_data:

  data frame, contains the odorant information.

- weightGlobNorm:

  data matrix, indicates whether given receptor has been measured by
  given study.

- responseRange:

  data frame, contains the information about response range of each
  study and how many odors have been measured in each study.

- receptors:

  data frame, contains the receptor and OSN names and their expression.

- ident:

  the identifier used for matching, usually the InChIKey is used.

- round:

  the number of digits the imported values are rounded to.

## Details

`import_new_data` is used to import new data into database. If the data
contains a new receptor or ORN, then build a new data frame for this
receptor or ORN. If the data contains a receptor that is already present
in database, then merge the imported data into old data frame. The
information (e.g. response range, how many receptors and odors were
measured from given study) will be integrated into data
`door_response_range`, `odor`, `ORs` and
`door_global_normalization_weights`. If an existing study is imported,
[`remove_study`](https://docs.ropensci.org/DoOR.functions/reference/remove_study.md)
will be run first in order to perform an update.

Stops if it finds any duplicates in the identifier columns, omits NAs on
check.

## Author

Shouwen Ma \<<shouwen.ma@uni-konstanz.de>\>

Daniel Münch \<<daniel.muench@uni-konstanz.de>\>

## Examples
