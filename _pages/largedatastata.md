---
layout: page
permalink: /largedatastata/
title: Working with "large" data in Stata
description: A collection of tips, prompted by discussions at the <a href='https://sa-tied.wider.unu.edu/data'>South African National Treasury Secure Data Facility (NT-SDF)</a>.
nav: false
---

* When using a shared resource (e.g. a server):
    - Make sure you `clear` your dataset when your analysis is finished running, if your dataset is large relative to the amount of memory available on the server. Holding large datasets in memory while not actively using them is a sin!
    - Be considerate if you're running computationally/memory intensive tasks which use excessive shared resources. Inefficient code in this case is not just a tax on your time, but a tax on all other users' time too. You may want to consider running the analysis on a subsample of the data, and then running the full analysis over a weekend or night when other users are less affected (see `help sample`, note the `by()` option).  
<br>
* Use the [Gtools suite of commands](https://gtools.readthedocs.io/en/latest/) (`help gtools`) instead of the native Stata equivalents. These include `gegen`, `gcollapse`, `gduplicates`, `glevelsof`, `gunique`, `gdistinct` and more, which are all essentially (much) faster versions of the original Stata commands and simply replace the original commands in your code. It's worth checking their website or reading the help file for each command to get maximum benefits (there are often `gtools`-specific additions/options you can use), but this is not necessary.  

* If running fixed effects regressions, especially with many fixed effects, use [Sergio Correia's](http://scorreia.com/software/reghdfe/) `reghdfe`. To get the computational benefits make sure the fixed effects are specified inside the `absorb()` option. In the (very few) cases where `reghdfe` is inappropriate, you might want to use `areg`. `xtreg, fe` is **extremely** slow with many fixed effects and large datasets.  
    - If you need to estimate a large number of fixed effects (or something else) for use in subsequent analysis -- save them in a dataset for use later, don't re-estimate the whole model each time!  
<br>
* For quantiles: `fastxtile`, `fasterxtile`, `gquantile`  

* Familiarise yourself with Stata variable [storage types](https://povertyaction.github.io/guides/cleaning/variablemanagement/storagetypes/). You do not want to hold variables in inefficient storage types which take up unnecessary memory, but on the other hand precision issues can also bite in large datasets if you are not careful in how ID variables are created and managed.
    - Avoid strings as much as possible: they take up a huge amount of memory if you have many observations and/or the strings are long. It is often better to `encode` strings and save them as categorical numeric variables with value labels. 
    - ID variables can also be converted to numeric variables, saving space and helping with commands like `xtset`, but typically not via `encode`. In this case use `gegen group` (`help gegen`). But take care when doing this: for ID variables it is essential that you declare the data type to retain precision. Often a "long" data type is sufficient, e.g. `gegen long firmID = group(stringID)` but check digits of accuracy [here](https://povertyaction.github.io/guides/cleaning/06%20Coding%20in%20Stata/02%20Numerical%20Formats/); you may need to declare the type as "double", at the expense of using more memory again. Note that the numeric ID variable will only be unique within the dataset it is created. Do not use for merging or after appending data. 
    - In general it is useful to declare the data type when creating variables if you know what is appropriate. E.g. for a dummy variable: `gen byte female = gender == 2 if !mi(gender)`.
    - If you are using dates, using Stata's native date functions (`help datetime`) can offer substantial improvements over using strings or other workarounds.  
<br>
* **ALWAYS** `compress` your data before saving. This recasts variables into the smallest data type which preserves precision.  

* `if` conditions are slow. If you are repetitively performing analysis on a subset of the data, it is often better to subset the data beforehand with `keep` (which can be combined with frames, `preserve`/`restore`, tempfiles if the subset is only used temporarily). In general you may experience substantial speed improvements by reducing the dataset to what you need for analysis rather than running the analysis on a large dataset with extraneous variables/observations.  

* `merge` can be slow, but a substantial part of this is the internal `sort` used to merge. If you consistently sort your data in a particular way before saving, and merge on the same hierarchy of variables, your merges will be quicker. And don't `sort` needlessly!  

* Avoid `gsort`, which can be incredibly slow. If you need a descending sort, it is quicker to generate a negative version of the variable you're sorting on, and sort on that.  

* In general if you have to use a very slow command (e.g `reshape`) try to do it once and save the resulting dataset (or just a subset for a `merge`) for re-use rather than re-running the time-intensive command again and again every time you need that particular dataset.  

* `codebook` is extremely slow. For numeric variables, a much quicker option to get a sense of a variable is `inspect`. If you want the number of unique values of a variable, use `gdistinct` or `gunique`. `gstats` provides a number of useful commands for quick summary statistics (`help gstats`).

* Loading a large dataset takes time. Frames typically provide a speed improvement over `preserve`/`restore` or using tempfiles.  

* `recode` is slow; a more cumbersone `replace if...` workflow is usually better in terms of computation time. But your programming time also matters!  
 
* `use` `varlist` `if` when loading a subset of a dataset can save time compared to loading and then dropping (`help use`).