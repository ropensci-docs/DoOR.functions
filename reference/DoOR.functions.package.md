# DoOR Functions

Functions package providing manipulation and application of the DoOR.

## Details

|           |                |
|-----------|----------------|
| Package:  | DoOR.functions |
| Type:     | Package        |
| Version:  | 2.0.0          |
| Date:     | 2016-01-25     |
| License:  | GPL-3          |
| LazyLoad: | yes            |

**Type
[`help(package = DoOR.functions)`](https://docs.ropensci.org/DoOR.functions/reference)
to see a complete list of datasets and functions. Below is what you need
for a quick start.**

First, load the DoOR packages, data and function package:

|  |  |
|----|----|
| [`library(DoOR.functions)`](https://docs.ropensci.org/DoOR.functions): |  |
| [`library(DoOR.data)`](https://docs.ropensci.org/DoOR.data): |  |

then, load all datasets including the precomputed response matrix:

|  |  |
|----|----|
| `load_door_data`: | Load all data into current active environment (function comes with DoOR.data) . |

or, load all odorant reseponse data into a list:

|  |  |
|----|----|
| [`load2list`](https://docs.ropensci.org/DoOR.functions/reference/load2list.md): | Load odorant response data only and compose them as a list. |

Try some visualizations (e.g. producing the plots from the paper):

|  |  |
|----|----|
| [`dplot_al_map`](https://docs.ropensci.org/DoOR.functions/reference/dplot_al_map.md): | response to a chemical mapped onto an image of the antennal lobe. |
| [`dplot_compare_profiles`](https://docs.ropensci.org/DoOR.functions/reference/dplot_compare_profiles.md): | compare the results of two studies. |
| [`dplot_response_matrix`](https://docs.ropensci.org/DoOR.functions/reference/dplot_response_matrix.md): | Dot Plot of Odorant Responses Across Receptors. |
| [`dplot_response_profile`](https://docs.ropensci.org/DoOR.functions/reference/dplot_response_profile.md): | bar plot: one receptor, all chemicals. |
| [`dplot_tuningCurve`](https://docs.ropensci.org/DoOR.functions/reference/dplot_tuningCurve.md): | pyramid diagram depicting a receptor's tuning breadth. |

Try some queries:

|  |  |
|----|----|
| [`get_responses`](https://docs.ropensci.org/DoOR.functions/reference/get_responses.md): | given a chemical, get original responses from all studies in the database. |
| [`get_normalized_responses`](https://docs.ropensci.org/DoOR.functions/reference/get_normalized_responses.md): | given a chemical, get normalised responses from all studies in the database. |

In case you wish to create your own response model (e.g. because you
want to include your own datasets):

|  |  |
|----|----|
| [`create_door_database`](https://docs.ropensci.org/DoOR.functions/reference/create_door_database.md): | compute the complete response model for all receptors in the database (calls [`model_response`](https://docs.ropensci.org/DoOR.functions/reference/model_response.md) for all receptors). |
| [`model_response`](https://docs.ropensci.org/DoOR.functions/reference/model_response.md): | run the DoOR algorithm, that merges all measurements for one receptor. |

Estimate odorant responses:

|  |  |
|----|----|
| [`estimate_missing_value`](https://docs.ropensci.org/DoOR.functions/reference/estimate_missing_value.md): | estimate NA entries in a consensus response data. |

Project the model response values back to tested values:

|  |  |
|----|----|
| [`back_project`](https://docs.ropensci.org/DoOR.functions/reference/back_project.md): | project the model response values back to tested values. |

Introduce new data into DoOR and update the supported data sets:

|  |  |
|----|----|
| [`import_new_data`](https://docs.ropensci.org/DoOR.functions/reference/import_new_data.md): | import new data into DoOR, and update the weight, response range and receptor names. |
| [`update_door_database`](https://docs.ropensci.org/DoOR.functions/reference/update_door_database.md): | update response matrix by calculating new consensus response data for a given receptor. |

See the Vignettes and the help pages for more documentation.

## References

<http://neuro.uni-konstanz.de/DoOR>

## See also

`DoOR.data`

## Author

C. Giovanni Galizia  
Daniel Muench  
Martin Strauch  
Anja Nissler  
Shouwen Ma  

Maintainer: Daniel Münch \<daniel.muench@uni-konstanz.de\>
