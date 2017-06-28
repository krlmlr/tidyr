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

|package   |*  |version   |date       |source                       |
|:---------|:--|:---------|:----------|:----------------------------|
|covr      |   |3.0.0     |2017-06-26 |CRAN (R 3.4.0)               |
|dplyr     |   |0.7.1     |2017-06-22 |cran (@0.7.1)                |
|gapminder |   |0.2.0     |2015-12-31 |cran (@0.2.0)                |
|knitr     |   |1.16      |2017-05-18 |cran (@1.16)                 |
|lazyeval  |   |0.2.0     |2016-06-12 |cran (@0.2.0)                |
|magrittr  |   |1.5       |2014-11-22 |CRAN (R 3.4.0)               |
|Rcpp      |   |0.12.11.2 |2017-06-05 |local                        |
|rmarkdown |   |1.6       |2017-06-15 |cran (@1.6)                  |
|stringi   |   |1.1.5     |2017-04-07 |cran (@1.1.5)                |
|testthat  |   |1.0.2     |2016-04-23 |cran (@1.0.2)                |
|tibble    |   |1.3.3     |2017-05-28 |cran (@1.3.3)                |
|tidyr     |   |0.6.3     |2017-06-27 |local (krlmlr/tidyr@1c77c76) |

# Check results

27 packages with problems

|package      |version   | errors| warnings| notes|
|:------------|:---------|------:|--------:|-----:|
|broom        |0.4.2     |      2|        0|     1|
|congressbr   |0.1.1     |      0|        1|     0|
|dartR        |0.80      |      0|        1|     0|
|emil         |2.2.6     |      1|        0|     1|
|eurostat     |3.1.1     |      0|        1|     0|
|eyetrackingR |0.1.6     |      2|        0|     0|
|flextable    |0.2.0     |      0|        1|     0|
|ggfortify    |0.4.1     |      2|        1|     1|
|harrietr     |0.2.2     |      1|        0|     0|
|highcharter  |0.5.0     |      1|        0|     1|
|lplyr        |0.1.6     |      1|        1|     0|
|MANOVA.RM    |0.0.5     |      0|        1|     1|
|metaplot     |0.1.2     |      1|        0|     0|
|NFP          |0.99.2    |      0|        1|     2|
|nonmemica    |0.7.1     |      0|        1|     1|
|nzelect      |0.3.3     |      0|        1|     0|
|officer      |0.1.4     |      2|        1|     0|
|padr         |0.3.0     |      1|        0|     0|
|qdap         |2.2.5     |      1|        0|     0|
|RSDA         |2.0       |      1|        0|     0|
|rtable       |0.1.5     |      1|        0|     0|
|shazam       |0.1.7     |      1|        2|     0|
|SWMPr        |2.2.0     |      1|        0|     0|
|tidyquant    |0.5.1     |      1|        0|     1|
|tigger       |0.2.9.999 |      0|        1|     0|
|unpivotr     |0.1.1     |      1|        0|     0|
|wrswoR       |1.0-1     |      0|        1|     1|

## broom (0.4.2)
Maintainer: David Robinson <admiral.david@gmail.com>  
Bug reports: http://github.com/tidyverse/broom/issues

2 errors | 0 warnings | 1 note 

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

checking R code for possible problems ... NOTE

 *** caught segfault ***
address 0x900000026, cause 'memory not mapped'

Traceback:
 1: collectUsageFun(name, formals(fun), body(fun), w)
 2: collectUsage(fun, enterGlobal = enter)
 3: codetools::findGlobals(v)
 4: FUN(X[[i]], ...)
 5: lapply(objects_in_env, function(v) {    if (typeof(v) == "closure")         codetools::findGlobals(v)})
 6: find_bad_closures(code_env)
 7: tools:::.check_depdef(package = "broom", WINDOWS = FALSE)
An irrecoverable exception occurred. R is aborting now ...
Segmentation fault (core dumped)
```

## congressbr (0.1.1)
Maintainer: Robert Myles McDonnell <robertmylesmcdonnell@gmail.com>

0 errors | 1 warning  | 0 notes

```
checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...
Loading required package: dplyr

Attaching package: 'dplyr'

The following objects are masked from 'package:stats':

    filter, lag

The following objects are masked from 'package:base':

    intersect, setdiff, setequal, union

Quitting from lines 44-47 (senate.Rmd) 
Error: processing vignette 'senate.Rmd' failed with diagnostics:
Column `senator_bills_details` must be length 1 or 93, not 92
Execution halted

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
27 Jun 21:42    Test set test_fraction 1 of 3 (0.7)
27 Jun 21:42      Evaluating modeling performance...
27 Jun 21:42    Test set test_fraction 2 of 3 (0.5)
27 Jun 21:42      Evaluating modeling performance...
27 Jun 21:42    Test set test_fraction 3 of 3 (0.3)
27 Jun 21:42      Evaluating modeling performance...
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
Attaching package: 'dplyr'

The following objects are masked from 'package:stats':

    filter, lag

The following objects are masked from 'package:base':
... 8 lines ...

Table ten00081 cached at /tmp/RtmpiwMq9i/eurostat/ten00081_date_code_TF.rds
trying URL 'http://ec.europa.eu/eurostat/estat-navtree-portlet-prod/BulkDownloadListing?sort=1&file=data%2Ftgs00026.tsv.gz'
Content type 'application/octet-stream;charset=UTF-8' length 4255 bytes
==================================================
downloaded 4255 bytes

Quitting from lines 310-336 (eurostat_tutorial.Rmd) 
Error: processing vignette 'eurostat_tutorial.Rmd' failed with diagnostics:
Evaluation error: only 0's may be mixed with negative subscripts.
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
  Running ‘testthat.R’ [104m/106m]
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
  Running ‘test-all.R’
Running the tests in ‘tests/test-all.R’ failed.
Last 13 lines of output:
  16: eval(exprs, env)
  17: source_file(path, new.env(parent = env), chdir = TRUE)
  18: force(code)
  19: with_reporter(reporter = reporter, start_end_reporter = start_end_reporter,     {        lister$start_file(basename(path))        source_file(path, new.env(parent = env), chdir = TRUE)        end_context()    })
  20: FUN(X[[i]], ...)
  21: lapply(paths, test_file, env = env, reporter = current_reporter,     start_end_reporter = FALSE, load_helpers = FALSE)
  22: force(code)
  23: with_reporter(reporter = current_reporter, results <- lapply(paths,     test_file, env = env, reporter = current_reporter, start_end_reporter = FALSE,     load_helpers = FALSE))
  24: test_files(paths, reporter = reporter, env = env, ...)
  25: test_dir(test_path, reporter = reporter, env = env, filter = filter,     ...)
  26: with_top_env(env, {    test_dir(test_path, reporter = reporter, env = env, filter = filter,         ...)})
  27: run_tests(package, test_path, filter, reporter, ...)
  28: test_check("ggfortify")
  An irrecoverable exception occurred. R is aborting now ...
  Segmentation fault (core dumped)

checking re-building of vignette outputs ... WARNING
Error in re-building vignettes:
  ...
 4: eval(expr, envir, enclos)
 5: withVisible(eval(expr, envir, enclos))
 6: withCallingHandlers(withVisible(eval(expr, envir, enclos)), warning = wHandler,     error = eHandler, message = mHandler)
 7: handle(ev <- withCallingHandlers(withVisible(eval(expr, envir,     enclos)), warning = wHandler, error = eHandler, message = mHandler))
 8: timing_fn(handle(ev <- withCallingHandlers(withVisible(eval(expr,     envir, enclos)), warning = wHandler, error = eHandler, message = mHandler)))
 9: evaluate_call(expr, parsed$src[[i]], envir = envir, enclos = enclos,     debug = debug, last = i == length(out), use_try = stop_on_error !=         2L, keep_warning = keep_warning, keep_message = keep_message,     output_handler = output_handler, include_timing = include_timing)
10: evaluate(code, envir = env, new_device = FALSE, keep_warning = !isFALSE(options$warning),     keep_message = !isFALSE(options$message), stop_on_error = if (options$error &&         options$include) 0L else 2L, output_handler = knit_handlers(options$render,         options))
... 8 lines ...
18: knit(input, text = text, envir = envir, encoding = encoding,     quiet = quiet)
19: knit2html(..., force_v1 = TRUE)
20: (if (grepl("\\.[Rr]md$", file)) knit2html_v1 else if (grepl("\\.[Rr]rst$",     file)) knit2pandoc else knit)(file, encoding = encoding,     quiet = quiet, envir = globalenv())
21: engine$weave(file, quiet = quiet, encoding = enc)
22: doTryCatch(return(expr), name, parentenv, handler)
23: tryCatchOne(expr, names, parentenv, handlers[[1L]])
24: tryCatchList(expr, classes, parentenv, handlers)
25: tryCatch({    engine$weave(file, quiet = quiet, encoding = enc)    setwd(startdir)    find_vignette_product(name, by = "weave", engine = engine)}, error = function(e) {    stop(gettextf("processing vignette '%s' failed with diagnostics:\n%s",         file, conditionMessage(e)), domain = NA, call. = FALSE)})
26: buildVignettes(dir = "/home/muelleki/git/R/tidyr/revdep/checks/ggfortify.Rcheck/vign_test/ggfortify")
An irrecoverable exception occurred. R is aborting now ...
Segmentation fault (core dumped)

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

## highcharter (0.5.0)
Maintainer: Joshua Kunst <jbkunst@gmail.com>  
Bug reports: https://github.com/jbkunst/highcharter/issues

1 error  | 0 warnings | 1 note 

```
checking examples ... ERROR
Running examples in ‘highcharter-Ex.R’ failed
The error most likely occurred in:

> base::assign(".ptime", proc.time(), pos = "CheckExEnv")
> ### Name: hcboxplot
> ### Title: Shortcut to make a boxplot
> ### Aliases: hcboxplot
> 
> ### ** Examples
> 
> hcboxplot(x = iris$Sepal.Length, var = iris$Species, color = "red")
Error in mutate_impl(.data, dots) : 
  Column `data` must be length 1 (the group size), not 5
Calls: hcboxplot ... transmute.default -> mutate -> mutate.tbl_df -> mutate_impl -> .Call
Execution halted

checking installed package size ... NOTE
  installed size is 16.5Mb
  sub-directories of 1Mb or more:
    doc          13.7Mb
    htmlwidgets   1.9Mb
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
  Running ‘testthat.R’ [49s/50s]
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
  Running ‘testthat.R’ [25s/26s]
Running the tests in ‘tests/testthat.R’ failed.
Last 13 lines of output:
                                                                ^
  tests/testthat/test-unnest.R:49:40: style: Commas should always have a space after.
    df <- data_frame(x = 1:3, y = list(1,2:3,4))
                                         ^
  tests/testthat/test-unnest.R:49:44: style: Commas should always have a space after.
    df <- data_frame(x = 1:3, y = list(1,2:3,4))
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
address 0xb4d0, cause 'memory not mapped'

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

## tidyquant (0.5.1)
Maintainer: Matt Dancho <mdancho@business-science.io>  
Bug reports: https://github.com/business-science/tidyquant/issues

1 error  | 0 warnings | 1 note 

```
checking tests ... ERROR
  Running ‘testthat.R’ [21s/51s]
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

Terminated

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

