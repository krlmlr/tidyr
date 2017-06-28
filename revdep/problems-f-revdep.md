# Setup

## Platform

|setting  |value                        |
|:--------|:----------------------------|
|version  |R version 3.4.0 (2017-04-21) |
|system   |x86_64, linux-gnu            |
|ui       |X11                          |
|language |(EN)                         |
|collate  |en_US.UTF-8                  |
|tz       |Zulu                         |
|date     |2017-06-28                   |

## Packages

|package    |*  |version    |date       |source                                |
|:----------|:--|:----------|:----------|:-------------------------------------|
|covr       |   |3.0.0      |2017-06-26 |CRAN (R 3.4.0)                        |
|dplyr      |   |0.7.1      |2017-06-22 |cran (@0.7.1)                         |
|gapminder  |   |0.2.0      |2015-12-31 |cran (@0.2.0)                         |
|glue       |   |1.1.1      |2017-06-21 |CRAN (R 3.4.0)                        |
|knitr      |   |1.16       |2017-05-18 |cran (@1.16)                          |
|magrittr   |   |1.5        |2014-11-22 |CRAN (R 3.4.0)                        |
|purrr      |   |0.2.2.2    |2017-05-11 |cran (@0.2.2.2)                       |
|Rcpp       |   |0.12.11.2  |2017-06-05 |local                                 |
|rlang      |   |0.1.1      |2017-05-18 |cran (@0.1.1)                         |
|rmarkdown  |   |1.6        |2017-06-15 |cran (@1.6)                           |
|stringi    |   |1.1.5      |2017-04-07 |cran (@1.1.5)                         |
|testthat   |   |1.0.2      |2016-04-23 |cran (@1.0.2)                         |
|tibble     |   |1.3.3      |2017-05-28 |cran (@1.3.3)                         |
|tidyr      |   |0.6.3.9000 |2017-06-28 |local (krlmlr/tidyr@1c4f781)          |
|tidyselect |   |0.0.0.9000 |2017-06-27 |Github (tidyverse/tidyselect@877968c) |

# Check results

42 packages with problems

|package        |version   | errors| warnings| notes|
|:--------------|:---------|------:|--------:|-----:|
|broom          |0.4.2     |      2|        0|     0|
|cdata          |0.1.1     |      2|        1|     0|
|d3r            |0.6.6     |      1|        0|     1|
|dartR          |0.80      |      0|        1|     0|
|emil           |2.2.6     |      1|        0|     1|
|eurostat       |3.1.1     |      0|        1|     0|
|explor         |0.3.2     |      1|        0|     0|
|eyetrackingR   |0.1.6     |      2|        0|     0|
|flextable      |0.2.0     |      0|        1|     0|
|fuzzyjoin      |0.1.3     |      2|        0|     0|
|ggfortify      |0.4.1     |      2|        1|     1|
|harrietr       |0.2.2     |      1|        0|     0|
|HTSSIP         |1.1.1     |      2|        1|     0|
|lans2r         |1.0.5     |      1|        1|     0|
|lplyr          |0.1.6     |      1|        1|     0|
|mafs           |0.0.2     |      1|        0|     0|
|MANOVA.RM      |0.0.5     |      0|        1|     1|
|metaplot       |0.1.2     |      1|        0|     0|
|mtconnectR     |1.1.0     |      2|        1|     0|
|NFP            |0.99.2    |      0|        1|     2|
|nonmemica      |0.7.1     |      0|        1|     1|
|nzelect        |0.3.3     |      0|        1|     0|
|officer        |0.1.4     |      2|        1|     0|
|padr           |0.3.0     |      1|        0|     0|
|qdap           |2.2.5     |      1|        0|     0|
|R6Frame        |0.1.0     |      1|        0|     0|
|radiant.basics |0.8.0     |      1|        0|     0|
|rfishbase      |2.1.2     |      1|        1|     0|
|rollply        |0.5.0     |      0|        1|     1|
|RSDA           |2.0       |      1|        0|     0|
|rtable         |0.1.5     |      1|        0|     0|
|rtdists        |0.7-3     |      0|        1|     0|
|sf             |0.5-1     |      1|        0|     1|
|shazam         |0.1.7     |      1|        2|     0|
|SWMPr          |2.2.0     |      1|        0|     0|
|textreuse      |0.1.4     |      2|        0|     1|
|tidygenomics   |0.1.0     |      2|        1|     0|
|tidyquant      |0.5.1     |      1|        0|     1|
|tigger         |0.2.9.999 |      0|        1|     0|
|unpivotr       |0.1.1     |      1|        0|     0|
|wrswoR         |1.0-1     |      0|        1|     1|
|WRTDStidal     |1.1.0     |      1|        0|     0|

## broom (0.4.2)
Maintainer: David Robinson <admiral.david@gmail.com>  
Bug reports: http://github.com/tidyverse/broom/issues

2 errors | 0 warnings | 0 notes

```
checking examples ... ERROR
Running examples in ‘broom-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: gmm_tidiers
> ### Title: Tidying methods for generalized method of moments "gmm" objects
> ### Aliases: glance.gmm gmm_tidiers tidy.gmm
> 
> ### ** Examples
... 58 lines ...
+     mutate(variable = reorder(variable, estimate)) %>%
+     ggplot(aes(estimate, variable)) +
+     geom_point() +
+     geom_errorbarh(aes(xmin = conf.low, xmax = conf.high)) +
+     facet_wrap(~ term) +
+     geom_vline(xintercept = 0, color = "red", lty = 2)
+ }
Error in `colnames<-`(`*tmp*`, value = c("conf.low", "conf.high")) : 
  attempt to set 'colnames' on an object with less than two dimensions
Calls: tidy -> tidy.gmm -> process_lm -> colnames<-
Execution halted

checking tests ... ERROR
  Running ‘test-all.R’
Running the tests in ‘tests/test-all.R’ failed.
Complete output:
  > library(testthat)
  > test_check("broom")
  Loading required package: broom
  Error in lahman_df() : could not find function "lahman_df"
  Calls: test_check ... with_reporter -> force -> source_file -> eval -> eval -> tbl
  testthat results ================================================================
  OK: 621 SKIPPED: 0 FAILED: 0
  Execution halted
```

## cdata (0.1.1)
Maintainer: John Mount <jmount@win-vector.com>  
Bug reports: https://github.com/WinVector/cdata/issues

2 errors | 1 warning  | 0 notes

```
checking examples ... ERROR
Running examples in ‘cdata-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: moveValuesToRows
> ### Title: Move values from columns to rows (wrapper for 'tidyr::gather',
> ###   or anti-pivot).
> ### Aliases: moveValuesToRows
> 
> ### ** Examples
> 
> 
> d <- data.frame(AUC= 0.6, R2= 0.2)
> moveValuesToRows(d,
+                  nameForNewKeyColumn= 'meas',
+                  nameForNewValueColumn= 'val',
+                  columnsToTakeFrom= c('AUC', 'R2'))
Error: Variable context not set
Execution halted

checking tests ... ERROR
  Running ‘testthat.R’
Running the tests in ‘tests/testthat.R’ failed.
Last 13 lines of output:
  11: lapply(.x, .f, ...)
  12: FUN(X[[i]], ...)
  13: overscope_eval_next(overscope, expr) at /tmp/RtmpeXZSpX/devtools1efb767e784/rlang/R/eval-tidy.R:104
  14: dplyr::one_of(columnsToTakeFrom)
  15: keep %in% vars at /tmp/RtmpeXZSpX/devtools1efb7e6e5a02/dplyr/R/select-utils.R:118
  16: current_vars()
  17: cur_vars_env$selected %||% abort("Variable context not set") at /tmp/RtmpeXZSpX/devtools1efb7e6e5a02/dplyr/R/select-utils.R:46
  18: abort("Variable context not set") at /tmp/RtmpeXZSpX/devtools1efb767e784/rlang/R/operators.R:14
  
  testthat results ================================================================
  OK: 0 SKIPPED: 0 FAILED: 1
  1. Error: testRowColOps.R (@testRowColOps.R#9) 
  
  Error: testthat unit tests failed
  Execution halted

checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...
Quitting from lines 284-292 (RowsAndColumns.Rmd) 
Error: processing vignette 'RowsAndColumns.Rmd' failed with diagnostics:
Variable context not set
Execution halted

```

## d3r (0.6.6)
Maintainer: Kent Russell <kent.russell@timelyportfolio.com>  
Bug reports: https://github.com/timelyportfolio/d3r/issues

1 error  | 0 warnings | 1 note 

```
checking examples ... ERROR
Running examples in ‘d3r-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: d3_nest
> ### Title: Convert a 'data.frame' to a 'd3.js' Hierarchy
> ### Aliases: d3_nest
> 
> ### ** Examples
... 16 lines ...
    intersect, setdiff, setequal, union

> 
> titanic_df <- data.frame(Titanic)
> tit_tb <- titanic_df %>%
+   select(Class,Age,Survived,Sex,Freq) %>%
+   d3_nest(value_cols="Freq", root="titanic")
Error in overscope_eval_next(overscope, expr) : 
  object 'children' not found
Calls: %>% ... map -> lapply -> FUN -> overscope_eval_next -> .Call
Execution halted

checking package dependencies ... NOTE
Package which this enhances but not available for checking: ‘treemap’
```

## dartR (0.80)
Maintainer: Bernd Gruber <bernd.gruber@canberra.edu.au>

0 errors | 1 warning  | 0 notes

```
checking whether package ‘dartR’ can be installed ... WARNING
Found the following significant warnings:
  Warning: namespace ‘DBI’ is not available and has been replaced
See ‘/home/muelleki/git/R/tidyr/revdep/checks/dartR.Rcheck/00install.out’ for details.
```

## emil (2.2.6)
Maintainer: Christofer Backlin <emil@christofer.backlin.se>  
Bug reports: https://github.com/Molmed/emil/issues

1 error  | 0 warnings | 1 note 

```
checking examples ... ERROR
Running examples in ‘emil-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: learning_curve
> ### Title: Learning curve analysis
> ### Aliases: learning_curve
> 
> ### ** Examples
... 6 lines ...
28 Jun 05:29    Test set test_fraction 1 of 3 (0.7)
28 Jun 05:29      Evaluating modeling performance...
28 Jun 05:29    Test set test_fraction 2 of 3 (0.5)
28 Jun 05:29      Evaluating modeling performance...
28 Jun 05:29    Test set test_fraction 3 of 3 (0.3)
28 Jun 05:29      Evaluating modeling performance...
> plot(lc)
Error in select.list(., test_fraction = TRUE, fold = TRUE, method = TRUE,  : 
  unused arguments (test_fraction = TRUE, fold = TRUE, method = TRUE, performance = "error")
Calls: plot ... _fseq -> freduce -> withVisible -> <Anonymous> -> select
Execution halted

checking compiled code ... NOTE
File ‘emil/libs/emil.so’:
  Found no calls to: ‘R_registerRoutines’, ‘R_useDynamicSymbols’

It is good practice to register native routines and to disable symbol
search.

See ‘Writing portable packages’ in the ‘Writing R Extensions’ manual.
```

## eurostat (3.1.1)
Maintainer: Leo Lahti <leo.lahti@iki.fi>  
Bug reports: https://github.com/ropengov/eurostat/issues

0 errors | 1 warning  | 0 notes

```
checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...
Loading required package: xml2
trying URL 'http://ec.europa.eu/eurostat/estat-navtree-portlet-prod/BulkDownloadListing?sort=1&file=data%2Ftsdtr210.tsv.gz'
Content type 'application/octet-stream;charset=UTF-8' length 4136 bytes
==================================================
downloaded 4136 bytes

Quitting from lines 112-113 (eurostat_tutorial.Rmd) 
Error: processing vignette 'eurostat_tutorial.Rmd' failed with diagnostics:
<text>:1:5: unexpected ','
1: unit,
        ^
Execution halted

```

## explor (0.3.2)
Maintainer: Julien Barnier <julien.barnier@ens-lyon.fr>  
Bug reports: https://github.com/juba/explor/issues

1 error  | 0 warnings | 0 notes

```
checking tests ... ERROR
  Running ‘testthat.R’
Running the tests in ‘tests/testthat.R’ failed.
Complete output:
  > library(testthat)
  > library(explor)
  > 
  > test_check("explor")
  Error: Variable context not set
  testthat results ================================================================
  OK: 0 SKIPPED: 0 FAILED: 0
  Execution halted
```

## eyetrackingR (0.1.6)
Maintainer: Jacob Dink <jacobwdink@gmail.com>  
Bug reports: https://github.com/jwdink/eyetrackingR/issues

2 errors | 0 warnings | 0 notes

```
checking examples ... ERROR
Running examples in ‘eyetrackingR-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: analyze_time_clusters
> ### Title: Bootstrap analysis of time-clusters.
> ### Aliases: analyze_time_clusters analyze_time_clusters.time_cluster_data
> 
> ### ** Examples
... 16 lines ...
> response_time <- make_time_sequence_data(response_window, time_bin_size = 500, aois = "Animate", 
+                                          predictor_columns = "Sex")
> 
> time_cluster_data <- make_time_cluster_data(data = response_time, predictor_column = "SexM", 
+                          aoi = "Animate", test = "lmer", 
+                          threshold = 1.5, 
+                          formula = LogitAdjusted ~ Sex + (1|Trial) + (1|ParticipantName))
Error in UseMethod("analyze_time_bins") : 
  no applicable method for 'analyze_time_bins' applied to an object of class "data.frame"
Calls: make_time_cluster_data ... make_time_cluster_data.time_sequence_data -> do.call -> <Anonymous>
Execution halted

checking tests ... ERROR
  Running ‘testthat.R’ [105m/106m]
Running the tests in ‘tests/testthat.R’ failed.
Last 13 lines of output:
  Computing t.test for each time bin...
  Computing t.test for each time bin...
  `mutate_each()` is deprecated.
  Use `mutate_all()`, `mutate_at()` or `mutate_if()` instead.
  To map `funs` over a selection of variables, use `mutate_at()`
  Avg. window length in new data will be 5500
  Performing Trackloss Analysis...
  Will exclude trials whose trackloss proportion is greater than : 0.25
  	...removed  33  trials.
  Error in UseMethod("make_time_cluster_data") : 
    no applicable method for 'make_time_cluster_data' applied to an object of class "data.frame"
  Calls: test_check ... source_file -> eval -> eval -> make_time_cluster_data
  testthat results ================================================================
  OK: 38 SKIPPED: 0 FAILED: 0
  Execution halted
```

## flextable (0.2.0)
Maintainer: David Gohel <david.gohel@ardata.fr>  
Bug reports: https://github.com/davidgohel/flextable/issues

0 errors | 1 warning  | 0 notes

```
checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...
Loading required package: officer

Attaching package: 'dplyr'

The following objects are masked from 'package:stats':

    filter, lag

The following objects are masked from 'package:base':

    intersect, setdiff, setequal, union

Quitting from lines 280-293 (format.Rmd) 
Error: processing vignette 'format.Rmd' failed with diagnostics:
file.exists(src) is not TRUE
Execution halted

```

## fuzzyjoin (0.1.3)
Maintainer: David Robinson <admiral.david@gmail.com>

2 errors | 0 warnings | 0 notes

```
checking examples ... ERROR
Running examples in ‘fuzzyjoin-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: genome_join
> ### Title: Join two tables based on overlapping genomic intervals: both a
> ### Aliases: genome_join genome_inner_join genome_left_join
> ###   genome_right_join genome_full_join genome_semi_join genome_anti_join
> 
... 22 lines ...
> x2 <- data_frame(id2 = 1:4,
+                  chromosome = c("chr1", "chr2", "chr2", "chr1"),
+                  start = c(140, 210, 400, 300),
+                  end = c(160, 240, 415, 320))
> 
> # note that the the third and fourth items don't join (even though
> # 300-350 and 300-320 overlap) since the chromosomes are different:
> genome_inner_join(x1, x2, by = c("chromosome", "start", "end"))
Error in overscope_eval_next(overscope, expr) : object 'x_data' not found
Calls: genome_inner_join ... map -> lapply -> FUN -> overscope_eval_next -> .Call
Execution halted

checking tests ... ERROR
  Running ‘testthat.R’ [24s/24s]
Running the tests in ‘tests/testthat.R’ failed.
Last 13 lines of output:
  8: nest.data.frame(data, key = !(!key_col), !(!(!nest_cols))) at /home/muelleki/git/R/tidyr/R/nest.R:35
  9: unname(tidyselect::vars_select(names(data), ...)) at /home/muelleki/git/R/tidyr/R/nest.R:47
  10: tidyselect::vars_select(names(data), ...) at /home/muelleki/git/R/tidyr/R/nest.R:47
  11: map_if(ind_list, !is_helper, eval_tidy, data = names_list)
  12: map(.x[matches], .f, ...)
  13: lapply(.x, .f, ...)
  14: FUN(X[[i]], ...)
  15: overscope_eval_next(overscope, expr) at /tmp/RtmpeXZSpX/devtools1efb767e784/rlang/R/eval-tidy.R:104
  
  testthat results ================================================================
  OK: 218 SKIPPED: 0 FAILED: 1
  1. Error: Can join genomes on chromosomes and intervals (@test_genome_join.R#16) 
  
  Error: testthat unit tests failed
  Execution halted
```

## ggfortify (0.4.1)
Maintainer: Masaaki Horikoshi <sinhrks@gmail.com>  
Bug reports: https://github.com/sinhrks/ggfortify/issues

2 errors | 1 warning  | 1 note 

```
checking examples ... ERROR
Running examples in ‘ggfortify-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: gglagplot
> ### Title: Plot time series against lagged versions of themselves
> ### Aliases: gglagplot
> 
> ### ** Examples
> 
> gglagplot(AirPassengers)
Error: `x` must be a vector, not a ts object, do you want `stats::lag()`?
Execution halted

checking tests ... ERROR
  Running ‘test-all.R’ [57s/59s]
Running the tests in ‘tests/test-all.R’ failed.
Last 13 lines of output:
  8: eval_bare(dot$expr, dot$env) at /tmp/RtmpeXZSpX/devtools1efb767e784/rlang/R/dots.R:91
  9: lapply(seq(1:lags), .lag)
  10: FUN(X[[i]], ...)
  11: as.vector(lag(ts, k))
  12: lag(ts, k)
  13: bad_args("x", "must be a vector, not a ts object, do you want `stats::lag()`?") at /tmp/RtmpeXZSpX/devtools1efb7e6e5a02/dplyr/R/lead-lag.R:65
  14: glubort(fmt_args(args), ..., .envir = .envir) at /tmp/RtmpeXZSpX/devtools1efb7e6e5a02/dplyr/R/error.R:21
  15: .abort(text) at /tmp/RtmpeXZSpX/devtools1efb7e6e5a02/dplyr/R/error.R:51
  
  testthat results ================================================================
  OK: 1442 SKIPPED: 9 FAILED: 1
  1. Error: gglagplot (@test-tslib.R#103) 
  
  Error: testthat unit tests failed
  Execution halted

checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...
Loading required package: Matrix

Attaching package: 'Matrix'

The following object is masked from 'package:dlm':

    bdiag
... 8 lines ...

The following object is masked from 'package:cluster':

    votes.repub

Quitting from lines 138-139 (plot_pca.Rmd) 
Error: processing vignette 'plot_pca.Rmd' failed with diagnostics:
<text>:1:6: unexpected symbol
1: Hook of
         ^
Execution halted

checking installed package size ... NOTE
  installed size is  5.7Mb
  sub-directories of 1Mb or more:
    doc   5.0Mb
```

## harrietr (0.2.2)
Maintainer: Anders Gonçalves da Silva <andersgs@gmail.com>  
Bug reports: https://github.com/andersgs/harrietr/issues

1 error  | 0 warnings | 0 notes

```
checking package dependencies ... ERROR
Package required but not available: ‘ggtree’

See section ‘The DESCRIPTION file’ in the ‘Writing R Extensions’
manual.
```

## HTSSIP (1.1.1)
Maintainer: Nicholas Youngblut <nyoungb2@gmail.com>

2 errors | 1 warning  | 0 notes

```
checking examples ... ERROR
Running examples in ‘HTSSIP-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: phyloseq2table
> ### Title: Phyloseq conversion to a ggplot-formatted table
> ### Aliases: phyloseq2table
> 
> ### ** Examples
> 
> data(physeq_S2D1)
> # Including some columns from sample metadata
> df_OTU = phyloseq2table(physeq_S2D1,
+                         include_sample_data=TRUE,
+                         sample_col_keep=c('Buoyant_density', 'Substrate', 'Day'))
Error in parse(text = x) : <text>:1:3: unexpected symbol
1: 12C
      ^
Calls: phyloseq2table ... eval_bare -> .Call -> parse_expr -> parse_exprs -> parse
Execution halted

checking tests ... ERROR
  Running ‘testthat.R’ [81s/80s]
Running the tests in ‘tests/testthat.R’ failed.
Last 13 lines of output:
  20: map(dots, function(dot) eval_bare(dot$expr, dot$env)) at /tmp/RtmpeXZSpX/devtools1efb767e784/rlang/R/dots.R:91
  21: lapply(.x, .f, ...) at /tmp/RtmpeXZSpX/devtools1efb767e784/rlang/R/compat-purrr.R:10
  22: FUN(X[[i]], ...)
  23: eval_bare(dot$expr, dot$env) at /tmp/RtmpeXZSpX/devtools1efb767e784/rlang/R/dots.R:91
  24: parse_expr(x)
  25: parse_exprs(x) at /tmp/RtmpeXZSpX/devtools1efb767e784/rlang/R/parse.R:53
  26: parse(text = x) at /tmp/RtmpeXZSpX/devtools1efb767e784/rlang/R/parse.R:74
  
  testthat results ================================================================
  OK: 87 SKIPPED: 15 FAILED: 2
  1. Error: delta BD on rep3 dataset (@test-delta_BD.R#27) 
  2. Error: bootstrap iteration is working (@test-qSIP_atom_excess.R#34) 
  
  Error: testthat unit tests failed
  Execution halted

checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...
converting counts to integer mode
converting counts to integer mode
converting counts to integer mode
converting counts to integer mode
converting counts to integer mode
converting counts to integer mode
converting counts to integer mode
... 8 lines ...
converting counts to integer mode
converting counts to integer mode
converting counts to integer mode
converting counts to integer mode
converting counts to integer mode
Quitting from lines 102-106 (qSIP.Rmd) 
Error: processing vignette 'qSIP.Rmd' failed with diagnostics:
<text>:1:3: unexpected symbol
1: 12C
      ^
Execution halted
```

## lans2r (1.0.5)
Maintainer: Sebastian Kopf <sebastian.kopf@colorado.edu>  
Bug reports: https://github.com/KopfLab/lans2r/issues

1 error  | 1 warning  | 0 notes

```
checking tests ... ERROR
  Running ‘testthat.R’ [15s/15s]
Running the tests in ‘tests/testthat.R’ failed.
Last 13 lines of output:
  39: map_if(quos, is_helper, eval_tidy)
  40: map(.x[matches], .f, ...)
  41: lapply(.x, .f, ...)
  42: FUN(X[[i]], ...)
  43: overscope_eval_next(overscope, expr) at /tmp/RtmpeXZSpX/devtools1efb767e784/rlang/R/eval-tidy.R:104
  
  testthat results ================================================================
  OK: 110 SKIPPED: 0 FAILED: 4
  1. Error: test that calculate works properly (@test-calculations.R#23) 
  2. Error: test that calculate ratios works properly (@test-calculations.R#70) 
  3. Error: test that calculate abundances works properly (@test-calculations.R#98) 
  4. Error: test that calculate sums works properly (@test-calculations.R#128) 
  
  Error: testthat unit tests failed
  Execution halted

checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...

Attaching package: 'dplyr'

The following objects are masked from 'package:stats':

    filter, lag

The following objects are masked from 'package:base':

    intersect, setdiff, setequal, union

Quitting from lines 40-56 (lans2r-calculate.Rmd) 
Error: processing vignette 'lans2r-calculate.Rmd' failed with diagnostics:
non-numeric argument to binary operator
Execution halted

```

## lplyr (0.1.6)
Maintainer: Paul Poncet <paulponcet@yahoo.fr>  
Bug reports: https://github.com/paulponcet/lplyr/issues

1 error  | 1 warning  | 0 notes

```
checking examples ... ERROR
Running examples in ‘lplyr-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: mutate_.list
> ### Title: Dplyr verbs for lists and pairlists
> ### Aliases: mutate_.list mutate_.pairlist rename_.list rename_.pairlist
> ###   select_.list select_.pairlist transmute_.list transmute_.pairlist
> 
... 35 lines ...
[1] "alpha"

$x3[[2]]
[1] "beta"  "gamma"


> select(xs, -x3)
Error in select.list(xs, -x3) : 
  select.list() cannot be used non-interactively
Calls: select -> select.list
Execution halted

checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...

Attaching package: 'dplyr'

The following objects are masked from 'package:stats':

    filter, lag

The following objects are masked from 'package:base':

    intersect, setdiff, setequal, union


Attaching package: 'lplyr'

The following object is masked from 'package:dplyr':

    pull

Quitting from lines 22-30 (lplyr-vignette.Rmd) 
Error: processing vignette 'lplyr-vignette.Rmd' failed with diagnostics:
select.list() cannot be used non-interactively
Execution halted

```

## mafs (0.0.2)
Maintainer: Sillas Gonzaga <sillas.gonzaga@gmail.com>  
Bug reports: http://github.com/sillasgonzaga/mafs/issues

1 error  | 0 warnings | 0 notes

```
checking examples ... ERROR
Running examples in ‘mafs-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: gg_fit
> ### Title: Graphical results of forecast models
> ### Aliases: gg_fit
> 
> ### ** Examples
> 
> gg_fit(AirPassengers, 12, "snaive")
Error in parse(text = x) : <text>:1:10: unexpected symbol
1: Original Series
             ^
Calls: gg_fit ... eval_bare -> .Call -> parse_expr -> parse_exprs -> parse
Execution halted
```

## MANOVA.RM (0.0.5)
Maintainer: Sarah Friedrich <sarah.friedrich@uni-ulm.de>

0 errors | 1 warning  | 1 note 

```
checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...
 7: eval(expr, envir, enclos)
 8: withVisible(eval(expr, envir, enclos))
 9: withCallingHandlers(withVisible(eval(expr, envir, enclos)), warning = wHandler,     error = eHandler, message = mHandler)
10: handle(ev <- withCallingHandlers(withVisible(eval(expr, envir,     enclos)), warning = wHandler, error = eHandler, message = mHandler))
11: timing_fn(handle(ev <- withCallingHandlers(withVisible(eval(expr,     envir, enclos)), warning = wHandler, error = eHandler, message = mHandler)))
12: evaluate_call(expr, parsed$src[[i]], envir = envir, enclos = enclos,     debug = debug, last = i == length(out), use_try = stop_on_error !=         2L, keep_warning = keep_warning, keep_message = keep_message,     output_handler = output_handler, include_timing = include_timing)
13: evaluate(code, envir = env, new_device = FALSE, keep_warning = !isFALSE(options$warning),     keep_message = !isFALSE(options$message), stop_on_error = if (options$error &&         options$include) 0L else 2L, output_handler = knit_handlers(options$render,         options))
... 8 lines ...
21: knitr::knit(knit_input, knit_output, envir = envir, quiet = quiet,     encoding = encoding)
22: rmarkdown::render(file, encoding = encoding, quiet = quiet, envir = globalenv())
23: vweave_rmarkdown(...)
24: engine$weave(file, quiet = quiet, encoding = enc)
25: doTryCatch(return(expr), name, parentenv, handler)
26: tryCatchOne(expr, names, parentenv, handlers[[1L]])
27: tryCatchList(expr, classes, parentenv, handlers)
28: tryCatch({    engine$weave(file, quiet = quiet, encoding = enc)    setwd(startdir)    find_vignette_product(name, by = "weave", engine = engine)}, error = function(e) {    stop(gettextf("processing vignette '%s' failed with diagnostics:\n%s",         file, conditionMessage(e)), domain = NA, call. = FALSE)})
29: buildVignettes(dir = "/home/muelleki/git/R/tidyr/revdep/checks/MANOVA.RM.Rcheck/vign_test/MANOVA.RM")
An irrecoverable exception occurred. R is aborting now ...
Segmentation fault (core dumped)

checking Rd cross-references ... NOTE
Packages unavailable to check Rd xrefs: ‘GFD’, ‘nparLD’
```

## metaplot (0.1.2)
Maintainer: Tim Bergsma <bergsmat@gmail.com>

1 error  | 0 warnings | 0 notes

```
checking examples ... ERROR
Running examples in ‘metaplot-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: metaplot
> ### Title: Metaplot
> ### Aliases: metaplot metaplot.folded metaplot_.folded
> 
> ### ** Examples
... 62 lines ...
> 
> x %>% metaplot(AGE) # one continuous
> x %>% metaplot(PRED,DV) # two continuous
> x %>% metaplot(AGE,SEX) # continuous and categorical
> x %>% metaplot(SEX,AGE) # categorical and continuous
> x %>% metaplot(PRED,DV,SEX) # two continous and categorical
> x %>% metaplot(ETA1,ETA2,ETA3) # three or more continuous
Error in UseMethod("continuous") : 
  no applicable method for 'continuous' applied to an object of class "data.frame"
Calls: %>% ... corsplom.folded -> sapply -> lapply -> FUN -> continuous
Execution halted
```

## mtconnectR (1.1.0)
Maintainer: Subramanyam Ravishankar <subramanyam@systeminsights.com>

2 errors | 1 warning  | 0 notes

```
checking examples ... ERROR
Running examples in ‘mtconnectR-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: map_gcode_mtc
> ### Title: Create a mapping between simulated and actual data
> ### Aliases: map_gcode_mtc
> 
> ### ** Examples
> 
> data("example_gcode_parsed") # Parsed gcode
> data("example_mtc_device_3") # MTCDevice object of actual log data
> simulated_gcode_data = na.omit(simulate_data_from_gcode(example_gcode_parsed, 
+ start_time = 0, data_res = 0.1, data_type = "HH"))
> mtc_device_sim = create_mtc_device_from_ts(simulated_gcode_data)
> mtc_sim_mapped = map_gcode_mtc(mtc_device_sim, example_mtc_device_3, elasticity = 200)
Using the following mapping: 
  sim_name                                                 mtc_name
1    x_pos nist_testbed_GF_Agie_1<Device>:path_pos_x<PATH_POSITION>
2    y_pos nist_testbed_GF_Agie_1<Device>:path_pos_y<PATH_POSITION>
3    z_pos nist_testbed_GF_Agie_1<Device>:path_pos_z<PATH_POSITION>
Error: Variable context not set
Execution halted

checking tests ... ERROR
  Running ‘testthat.R’
Running the tests in ‘tests/testthat.R’ failed.
Last 13 lines of output:
    |===================================================================== |  99%
    |                                                                            
    |======================================================================|  99%
    |                                                                            
    |======================================================================| 100%
  93.43% data contextualized successfuly!
  Using the following mapping: 
    sim_name                                                 mtc_name
  1    x_pos nist_testbed_GF_Agie_1<Device>:path_pos_x<PATH_POSITION>
  2    y_pos nist_testbed_GF_Agie_1<Device>:path_pos_y<PATH_POSITION>
  3    z_pos nist_testbed_GF_Agie_1<Device>:path_pos_z<PATH_POSITION>
  Error: Variable context not set
  testthat results ================================================================
  OK: 0 SKIPPED: 0 FAILED: 0
  Execution halted

checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...
Quitting from lines 102-107 (simulate_map_gcode.Rmd) 
Error: processing vignette 'simulate_map_gcode.Rmd' failed with diagnostics:
Variable context not set
Execution halted

```

## NFP (0.99.2)
Maintainer: Yang Cao <yiluheihei@gmail.com>  
Bug reports: https://github.com/yiluheihei/NFP/issues

0 errors | 1 warning  | 2 notes

```
checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...
    clusterApply, clusterApplyLB, clusterCall, clusterEvalQ,
    clusterExport, clusterMap, parApply, parCapply, parLapply,
    parLapplyLB, parRapply, parSapply, parSapplyLB

The following objects are masked from 'package:stats':

    IQR, mad, sd, var, xtabs
... 8 lines ...
    pmin, pmin.int, rank, rbind, rowMeans, rowSums, rownames, sapply,
    setdiff, sort, table, tapply, union, unique, unsplit, which,
    which.max, which.min

Loading required package: graphite
Warning in library(package, lib.loc = lib.loc, character.only = TRUE, logical.return = TRUE,  :
  there is no package called 'graphite'
Quitting from lines 198-206 (NFP.Rnw) 
Error: processing vignette 'NFP.Rnw' failed with diagnostics:
could not find function "pathways"
Execution halted

checking package dependencies ... NOTE
Packages suggested but not available for checking: ‘graphite’ ‘NFPdata’

checking installed package size ... NOTE
  installed size is  8.2Mb
  sub-directories of 1Mb or more:
    data   7.5Mb
```

## nonmemica (0.7.1)
Maintainer: Tim Bergsma <bergsmat@gmail.com>

0 errors | 1 warning  | 1 note 

```
checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...
Segmentation fault (core dumped)


checking dependencies in R code ... NOTE
Segmentation fault (core dumped)
```

## nzelect (0.3.3)
Maintainer: Peter Ellis <peter.ellis2013nz@gmail.com>

0 errors | 1 warning  | 0 notes

```
checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...
Terminated

```

## officer (0.1.4)
Maintainer: David Gohel <david.gohel@ardata.fr>  
Bug reports: https://github.com/davidgohel/officer/issues

2 errors | 1 warning  | 0 notes

```
checking examples ... ERROR
Running examples in ‘officer-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: slip_in_img
> ### Title: append an image
> ### Aliases: slip_in_img
> 
> ### ** Examples
> 
> library(magrittr)
> img.file <- file.path( Sys.getenv("R_HOME"), "doc", "html", "logo.jpg" )
> x <- read_docx() %>%
+   body_add_par("R logo: ", style = "Normal") %>%
+   slip_in_img(src = img.file, style = "strong", width = .3, height = .3)
Error: file.exists(src) is not TRUE
Execution halted

checking tests ... ERROR
  Running ‘testthat.R’ [49s/49s]
Running the tests in ‘tests/testthat.R’ failed.
Last 13 lines of output:
  8: function_list[[k]](value) at /tmp/RtmpT6Czo8/R.INSTALL13c163d710cb/magrittr/R/freduce.R:20
  9: ph_with_img(., type = "body", src = img.file, height = 1.06, width = 1.39)
  10: external_img(src, width = width, height = height)
  11: stopifnot(file.exists(src))
  12: stop(msg, call. = FALSE, domain = NA)
  
  testthat results ================================================================
  OK: 343 SKIPPED: 0 FAILED: 4
  1. Error: image add  (@test-docx-add.R#76) 
  2. Error: pml fp_border (@test-fp_cell.R#75) 
  3. Error: css fp_border (@test-fp_cell.R#165) 
  4. Error: add img into placeholder (@test-pptx-add.R#67) 
  
  Error: testthat unit tests failed
  Execution halted

checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...

Attaching package: 'dplyr'

The following objects are masked from 'package:stats':

    filter, lag

The following objects are masked from 'package:base':

    intersect, setdiff, setequal, union

Quitting from lines 180-190 (powerpoint.Rmd) 
Error: processing vignette 'powerpoint.Rmd' failed with diagnostics:
file.exists(src) is not TRUE
Execution halted

```

## padr (0.3.0)
Maintainer: Edwin Thoen <edwinthoen@gmail.com>  
Bug reports: https://github.com/EdwinTh/padr/issues

1 error  | 0 warnings | 0 notes

```
checking tests ... ERROR
  Running ‘testthat.R’ [27s/27s]
Running the tests in ‘tests/testthat.R’ failed.
Last 13 lines of output:
                                                            ^
  tests/testthat/test-unnest.R:49:36: style: Commas should always have a space after.
    df <- tibble(x = 1:3, y = list(1,2:3,4))
                                     ^
  tests/testthat/test-unnest.R:49:40: style: Commas should always have a space after.
    df <- tibble(x = 1:3, y = list(1,2:3,4))
                                         ^
  
  
  testthat results ================================================================
  OK: 344 SKIPPED: 0 FAILED: 1
  1. Failure: Package Style (@test_zzz_lintr.R#5) 
  
  Error: testthat unit tests failed
  Execution halted
```

## qdap (2.2.5)
Maintainer: Tyler Rinker <tyler.rinker@gmail.com>  
Bug reports: http://github.com/trinker/qdap/issues

1 error  | 0 warnings | 0 notes

```
checking whether package ‘qdap’ can be installed ... ERROR
Installation failed.
See ‘/home/muelleki/git/R/tidyr/revdep/checks/qdap.Rcheck/00install.out’ for details.
```

## R6Frame (0.1.0)
Maintainer: Kristian D. Olsen <kristian@doingit.no>

1 error  | 0 warnings | 0 notes

```
checking tests ... ERROR
  Running ‘testthat.R’
Running the tests in ‘tests/testthat.R’ failed.
Last 13 lines of output:
  
  testthat results ================================================================
  OK: 140 SKIPPED: 0 FAILED: 9
  1. Error: gather works with R6 data.frame (@test-tidyr_reshape.R#11) 
  2. Error: gather works with R6 data.table (@test-tidyr_reshape.R#25) 
  3. Error: gather works with R6 tbl_df (@test-tidyr_reshape.R#38) 
  4. Error: spread works with R6 data.frame (@test-tidyr_reshape.R#52) 
  5. Error: spread works with R6 data.table (@test-tidyr_reshape.R#67) 
  6. Error: spread works with R6 tbl_df (@test-tidyr_reshape.R#81) 
  7. Error: complete works with R6 data.frame (@test-tidyr_verbs.R#13) 
  8. Error: complete works with R6 data.table (@test-tidyr_verbs.R#27) 
  9. Error: complete works with R6 tbl_df (@test-tidyr_verbs.R#41) 
  
  Error: testthat unit tests failed
  Execution halted
```

## radiant.basics (0.8.0)
Maintainer: Vincent Nijs <radiant@rady.ucsd.edu>  
Bug reports: https://github.com/radiant-rstats/radiant.basics/issues

1 error  | 0 warnings | 0 notes

```
checking examples ... ERROR
Running examples in ‘radiant.basics-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: plot.cross_tabs
> ### Title: Plot method for the cross_tabs function
> ### Aliases: plot.cross_tabs
> 
> ### ** Examples
> 
> result <- cross_tabs("newspaper", "Income", "Newspaper")
> plot(result, check = c("observed","expected","chi_sq"))
Error in parse(text = x) : <text>:1:4: unexpected symbol
1: WS Journal
       ^
Calls: plot ... _fseq -> freduce -> withVisible -> <Anonymous> -> sshhr
Execution halted
```

## rfishbase (2.1.2)
Maintainer: Carl Boettiger <cboettig@ropensci.org>  
Bug reports: https://github.com/ropensci/rfishbase/issues

1 error  | 1 warning  | 0 notes

```
checking tests ... ERROR
  Running ‘testthat.R’ [2s/12s]
Running the tests in ‘tests/testthat.R’ failed.
Last 13 lines of output:
         tidy_table(data, server = server)
     })
  10: FUN(X[[i]], ...)
  11: httr::GET(paste0(server, "/", endpt), query = args, httr::user_agent(make_ua()))
  12: request_perform(req, hu$handle$handle) at /tmp/RtmpC44KWe/R.INSTALL1cab52ce53dc/httr/R/http-get.r:67
  13: request_fetch(req$output, req$url, handle) at /tmp/RtmpC44KWe/R.INSTALL1cab52ce53dc/httr/R/request.R:133
  14: request_fetch.write_memory(req$output, req$url, handle) at /tmp/RtmpC44KWe/R.INSTALL1cab52ce53dc/httr/R/write-function.R:74
  15: curl::curl_fetch_memory(url, handle = handle) at /tmp/RtmpC44KWe/R.INSTALL1cab52ce53dc/httr/R/write-function.R:76
  
  testthat results ================================================================
  OK: 35 SKIPPED: 32 FAILED: 1
  1. Error: Custom queries give desired result (@test_endpoint.R#10) 
  
  Error: testthat unit tests failed
  Execution halted

checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...
Quitting from lines 69-70 (tutorial.Rmd) 
Error: processing vignette 'tutorial.Rmd' failed with diagnostics:
Timeout was reached
Execution halted

```

## rollply (0.5.0)
Maintainer: Alexandre Genin <alex@lecairn.org>  
Bug reports: https://github.com/alexgenin/rollply

0 errors | 1 warning  | 1 note 

```
checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...
Quitting from lines 51-60 (rollply.Rmd) 
Error: processing vignette 'rollply.Rmd' failed with diagnostics:
cannot open the connection to 'ftp://aftp.cmdl.noaa.gov/products/trends/co2/co2_mm_mlo.txt'
Execution halted


checking compiled code ... NOTE
File ‘rollply/libs/rollply.so’:
  Found no calls to: ‘R_registerRoutines’, ‘R_useDynamicSymbols’

It is good practice to register native routines and to disable symbol
search.

See ‘Writing portable packages’ in the ‘Writing R Extensions’ manual.
```

## RSDA (2.0)
Maintainer: Oldemar Rodriguez <oldemar.rodriguez@ucr.ac.cr>

1 error  | 0 warnings | 0 notes

```
checking examples ... ERROR
Running examples in ‘RSDA-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: classic.to.sym
> ### Title: Generate a symbolic data table
> ### Aliases: classic.to.sym
> ### Keywords: data symbolic table
> 
> ### ** Examples
> 
> data(ex1_db2so)
> ex1 <- ex1_db2so
> result <- classic.to.sym(ex1, concept=c('state', 'sex'),
+                          variables=c('county', 'group', 'age','age'),
+                          variables.types=c('$C', '$I', '$M', '$S'))
Loading required package: tcltk
Warning: no DISPLAY variable so Tk is not available
Error in rsqlite_send_query(conn@ptr, statement) : 
  no such table: main.dataTable
Calls: classic.to.sym ... initialize -> initialize -> rsqlite_send_query -> .Call
Execution halted
```

## rtable (0.1.5)
Maintainer: David Gohel <david.gohel@lysis-consultants.fr>  
Bug reports: https://github.com/davidgohel/rtable/issues

1 error  | 0 warnings | 0 notes

```
checking whether package ‘rtable’ can be installed ... ERROR
Installation failed.
See ‘/home/muelleki/git/R/tidyr/revdep/checks/rtable.Rcheck/00install.out’ for details.
```

## rtdists (0.7-3)
Maintainer: Henrik Singmann <singmann+rtdists@gmail.com>  
Bug reports: https://github.com/rtdists/rtdists/issues

0 errors | 1 warning  | 0 notes

```
checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...
The following objects are masked from 'package:stats':

    filter, lag

The following objects are masked from 'package:base':

    intersect, setdiff, setequal, union
... 8 lines ...

    contains, order_by

Loading required package: lattice
Loading required package: latticeExtra
Loading required package: RColorBrewer
Loading required package: binom
Quitting from lines 374-396 (reanalysis_rr98.Rmd) 
Error: processing vignette 'reanalysis_rr98.Rmd' failed with diagnostics:
Variable context not set
Execution halted
```

## sf (0.5-1)
Maintainer: Edzer Pebesma <edzer.pebesma@uni-muenster.de>  
Bug reports: https://github.com/edzer/sfr/issues/

1 error  | 0 warnings | 1 note 

```
checking tests ... ERROR
  Running ‘cast.R’
  Comparing ‘cast.Rout’ to ‘cast.Rout.save’ ...4c4
< Linking to GEOS 3.5.0, GDAL 2.1.0, proj.4 4.9.2
---
> Linking to GEOS 3.5.1, GDAL 2.1.3, proj.4 4.9.2
  Running ‘crs.R’
  Comparing ‘crs.Rout’ to ‘crs.Rout.save’ ... OK
  Running ‘dist.R’
  Comparing ‘dist.Rout’ to ‘dist.Rout.save’ ... OK
... 118 lines ...
  Dataset /home/muelleki/git/R/tidyr/revdep/checks/sf.Rcheck/tests/testthat/x.gpkg already exists: remove first, use update=TRUE to append,
  delete_layer=TRUE to delete layer, or delete_dsn=TRUE to remove the entire data source before writing.
  Creating layer . failed.
  Failed to create feature 1 in x
  Failed to create feature 1 in x
  testthat results ================================================================
  OK: 469 SKIPPED: 9 FAILED: 1
  1. Error: separate and unite work (@test_tidy.R#13) 
  
  Error: testthat unit tests failed
  Execution halted

checking installed package size ... NOTE
  installed size is 13.1Mb
  sub-directories of 1Mb or more:
    doc      4.0Mb
    libs     5.5Mb
    sqlite   1.5Mb
```

## shazam (0.1.7)
Maintainer: Jason Vander Heiden <jason.vanderheiden@yale.edu>  
Bug reports: https://bitbucket.org/kleinstein/shazam/issues

1 error  | 2 warnings | 0 notes

```
checking examples ... ERROR
Running examples in ‘shazam-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: calcBaseline
> ### Title: Calculate the BASELINe PDFs
> ### Aliases: calcBaseline
> 
> ### ** Examples
... 9 lines ...
+                          germlineColumn="GERMLINE_IMGT_D_MASK", 
+                          testStatistic="focused",
+                          regionDefinition=IMGT_V,
+                          targetingModel=HH_S5F,
+                          nproc=1)
Collapsing clonal sequences...
Error in dimnames(x) <- dn : 
  length of 'dimnames' [2] not equal to array extent
Calls: calcBaseline -> observedMutations -> colnames<-
Execution halted
** found \donttest examples: check also with --run-donttest

checking Rd cross-references ... WARNING
package ‘alakazam’ exists but was not installed under R >= 2.10.0 so xrefs cannot be checked

checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...
Loading required package: ggplot2
Quitting from lines 102-111 (Baseline-Vignette.Rmd) 
Error: processing vignette 'Baseline-Vignette.Rmd' failed with diagnostics:
The column GERMLINE_IMGT_D_MASK contains no data
Execution halted

```

## SWMPr (2.2.0)
Maintainer: Marcus W. Beck <mbafs2012@gmail.com>  
Bug reports: http://github.com/fawda123/SWMPr/issues

1 error  | 0 warnings | 0 notes

```
checking examples ... ERROR
Running examples in ‘SWMPr-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: plot_summary
> ### Title: Plot graphical summaries of SWMP data
> ### Aliases: plot_summary plot_summary.swmpr
> 
> ### ** Examples
... 10 lines ...
address 0x20400000306, cause 'memory not mapped'

Traceback:
 1: arrangeGrob(...)
 2: gridExtra::grid.arrange(arrangeGrob(p1, p2, ncol = 1), p3, arrangeGrob(p4,     p5, p6, ncol = 1, heights = c(1, 1, 0.8)), ncol = 3, widths = c(1,     0.5, 1))
 3: withCallingHandlers(expr, warning = function(w) invokeRestart("muffleWarning"))
 4: suppressWarnings(gridExtra::grid.arrange(arrangeGrob(p1, p2,     ncol = 1), p3, arrangeGrob(p4, p5, p6, ncol = 1, heights = c(1,     1, 0.8)), ncol = 3, widths = c(1, 0.5, 1)))
 5: plot_summary.swmpr(dat, param = "chla_n", years = c(2007, 2013))
 6: plot_summary(dat, param = "chla_n", years = c(2007, 2013))
An irrecoverable exception occurred. R is aborting now ...
Segmentation fault (core dumped)
```

## textreuse (0.1.4)
Maintainer: Lincoln Mullen <lincoln@lincolnmullen.com>  
Bug reports: https://github.com/ropensci/textreuse/issues

2 errors | 0 warnings | 1 note 

```
checking examples ... ERROR
Running examples in ‘textreuse-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: lsh
> ### Title: Locality sensitive hashing for minhash
> ### Aliases: lsh
> 
> ### ** Examples
> 
> dir <- system.file("extdata/legal", package = "textreuse")
> minhash <- minhash_generator(200, seed = 235)
> corpus <- TextReuseCorpus(dir = dir,
+                           tokenizer = tokenize_ngrams, n = 5,
+                           minhash_func = minhash)
> buckets <- lsh(corpus, bands = 50)
Error in overscope_eval_next(overscope, expr) : object 'ca1851' not found
Calls: lsh ... map -> lapply -> FUN -> overscope_eval_next -> .Call
Execution halted

checking tests ... ERROR
  Running ‘testthat.R’
Running the tests in ‘tests/testthat.R’ failed.
Complete output:
  > library(testthat)
  > library(textreuse)
  > 
  > test_check("textreuse")
  Error in overscope_eval_next(overscope, expr) : object 'ca1851' not found
  Calls: test_check ... map -> lapply -> FUN -> overscope_eval_next -> .Call
  testthat results ================================================================
  OK: 85 SKIPPED: 2 FAILED: 0
  Execution halted

checking compiled code ... NOTE
File ‘textreuse/libs/textreuse.so’:
  Found no calls to: ‘R_registerRoutines’, ‘R_useDynamicSymbols’

It is good practice to register native routines and to disable symbol
search.

See ‘Writing portable packages’ in the ‘Writing R Extensions’ manual.
```

## tidygenomics (0.1.0)
Maintainer: Constantin Ahlmann-Eltze <artjom31415@googlemail.com>

2 errors | 1 warning  | 0 notes

```
checking examples ... ERROR
Running examples in ‘tidygenomics-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: genome_complement
> ### Title: Calculates the complement to the intervals covered by the
> ###   intervals in a data frame. It can optionally take a 'chromosome_size'
> ###   data frame that contains 2 or 3 columns, the first the names of
> ###   chromosome and in case there are 2 columns the size or first the
... 18 lines ...

> 
> x1 <- data.frame(id = 1:4, bla=letters[1:4],
+                  chromosome = c("chr1", "chr1", "chr2", "chr1"),
+                  start = c(100, 200, 300, 400),
+                  end = c(150, 250, 350, 450))
> 
> genome_complement(x1, by=c("chromosome", "start", "end"))
Error in overscope_eval_next(overscope, expr) : object 'x_data' not found
Calls: genome_complement ... map -> lapply -> FUN -> overscope_eval_next -> .Call
Execution halted

checking tests ... ERROR
  Running ‘testthat.R’
Running the tests in ‘tests/testthat.R’ failed.
Last 13 lines of output:
  13: overscope_eval_next(overscope, expr) at /tmp/RtmpeXZSpX/devtools1efb767e784/rlang/R/eval-tidy.R:104
  
  testthat results ================================================================
  OK: 7 SKIPPED: 0 FAILED: 8
  1. Error: Calculating the complement of a sequence works (@test_complement.R#12) 
  2. Error: Intersection (both) of 2 data frames works as expected (@test_intersect.R#17) 
  3. Error: Intersection of 2 data frames works for multi-overlap ranges (@test_intersect.R#29) 
  4. Error: Intersection of 2 data frames works for multi-overlap ranges the other way around (@test_intersect.R#46) 
  5. Error: Joining with closest works as expected (@test_join_closest.R#17) 
  6. Error: Subtraction of 2 data frames works as expected (@test_subtract.R#18) 
  7. Error: Edge cases of subtraction of 2 data frames works as expected (@test_subtract.R#38) 
  8. Error: during subtraction the intervals are not unified (@test_subtract.R#57) 
  
  Error: testthat unit tests failed
  Execution halted

checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...

Attaching package: 'dplyr'

The following objects are masked from 'package:stats':

    filter, lag

The following objects are masked from 'package:base':

    intersect, setdiff, setequal, union

Quitting from lines 55-66 (intro.Rmd) 
Error: processing vignette 'intro.Rmd' failed with diagnostics:
object 'x_data' not found
Execution halted

```

## tidyquant (0.5.1)
Maintainer: Matt Dancho <mdancho@business-science.io>  
Bug reports: https://github.com/business-science/tidyquant/issues

1 error  | 0 warnings | 1 note 

```
checking tests ... ERROR
  Running ‘testthat.R’ [22s/50s]
Running the tests in ‘tests/testthat.R’ failed.
Last 13 lines of output:
  nrow(test2) not equal to 208.
  1/1 mismatches
  [1] 206 - 208 == -2
  
  
  testthat results ================================================================
  OK: 185 SKIPPED: 2 FAILED: 5
  1. Error: Test prints warning message on invalid x input. (@test_tq_get_dividends.R#23) 
  2. Error: Test returns NA on invalid x input. (@test_tq_get_dividends.R#27) 
  3. Failure: Test prints warning message on invalid x input. (@test_tq_get_splits.R#23) 
  4. Failure: Test 1 returns tibble with correct rows and columns. (@test_tq_get_stock_prices.R#19) 
  5. Failure: Test 2 returns tibble with correct rows and columns. (@test_tq_get_stock_prices.R#28) 
  
  Error: testthat unit tests failed
  Execution halted

checking installed package size ... NOTE
  installed size is  5.2Mb
  sub-directories of 1Mb or more:
    doc   4.5Mb
```

## tigger (0.2.9.999)
Maintainer: Daniel Gadala-Maria <daniel.gadala-maria@yale.edu>  
Bug reports: https://bitbucket.org/kleinstein/tigger/issues

0 errors | 1 warning  | 0 notes

```
checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...
Loading required package: ggplot2

Attaching package: 'dplyr'

The following objects are masked from 'package:stats':

    filter, lag

The following objects are masked from 'package:base':

    intersect, setdiff, setequal, union


 *** caught segfault ***
address 0x12, cause 'memory not mapped'
Segmentation fault (core dumped)

```

## unpivotr (0.1.1)
Maintainer: Duncan Garmonsway <nacnudus@gmail.com>  
Bug reports: https://github.com/nacnudus/unpivotr/issues

1 error  | 0 warnings | 0 notes

```
checking tests ... ERROR
  Running ‘testthat.R’
Running the tests in ‘tests/testthat.R’ failed.
Last 13 lines of output:
  
  The following objects are masked from 'package:stats':
  
      filter, lag
  
  The following objects are masked from 'package:base':
  
      intersect, setdiff, setequal, union
  
  testthat results ================================================================
  OK: 119 SKIPPED: 0 FAILED: 1
  1. Failure: 'cross' works (@test-anchor.R#19) 
  
  Error: testthat unit tests failed
  Execution halted
```

## wrswoR (1.0-1)
Maintainer: Kirill Müller <krlmlr+r@mailbox.org>  
Bug reports: https://github.com/krlmlr/wrswoR/issues

0 errors | 1 warning  | 1 note 

```
checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...
Quitting from lines 622-635 (wrswoR.Rmd) 
Error: processing vignette 'wrswoR.Rmd' failed with diagnostics:

TeX was unable to calculate metrics for the following string
or character:

	77

Common reasons for failure include:
  * The string contains a character which is special to LaTeX unless
    escaped properly, such as % or $.
  * The string makes use of LaTeX commands provided by a package and
    the tikzDevice was not told to load the package.

The contents of the LaTeX log of the aborted run have been printed above,
it may contain additional details as to why the metric calculation failed.
Execution halted


checking compiled code ... NOTE
File ‘wrswoR/libs/wrswoR.so’:
  Found no calls to: ‘R_registerRoutines’, ‘R_useDynamicSymbols’

It is good practice to register native routines and to disable symbol
search.

See ‘Writing portable packages’ in the ‘Writing R Extensions’ manual.
```

## WRTDStidal (1.1.0)
Maintainer: Marcus W. Beck <mbafs2012@gmail.com>  
Bug reports: https://github.com/fawda123/wtreg_for_estuaries/issues

1 error  | 0 warnings | 0 notes

```
checking examples ... ERROR
Running examples in ‘WRTDStidal-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: fitplot
> ### Title: Plot the fitted results for a tidal object
> ### Aliases: fitplot fitplot.tidal fitplot.tidalmean
> 
> ### ** Examples
> 
> 
> ## load a fitted tidal object
> data(tidfit)
> 
> # plot using defaults
> fitplot(tidfit)
Error: Variable context not set
Execution halted
```

