# afex

Version: 0.18-0

## Newly broken

*   checking Rd cross-references ... NOTE
    ```
    Packages unavailable to check Rd xrefs: ‘ez’, ‘ascii’
    ```

## Newly fixed

*   checking whether package ‘afex’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/afex/old/afex.Rcheck/00install.out’ for details.
    ```

# biobroom

Version: 1.8.0

## Newly broken

*   checking dependencies in R code ... NOTE
    ```
    'library' or 'require' call to ‘DESeq2’ in package code.
      Please use :: or requireNamespace() instead.
      See section 'Suggested packages' in the 'Writing R Extensions' manual.
    Missing or unexported object: ‘dplyr::tbl_dt’
    ```

*   checking R code for possible problems ... NOTE
    ```
    ...
      for ‘colData’
    tidy.deSet: no visible global function definition for ‘exprs<-’
    tidy.deSet: no visible binding for global variable ‘value’
    tidy.deSet: no visible binding for global variable ‘gene’
    tidy.deSet: no visible global function definition for ‘pData’
    tidy.qvalue: no visible binding for global variable ‘smoothed’
    tidy.qvalue: no visible binding for global variable ‘pi0’
    tidy.qvalue: no visible binding for global variable ‘lambda’
    tidy_matrix: no visible binding for global variable ‘value’
    tidy_matrix: no visible binding for global variable ‘gene’
    Undefined global functions or variables:
      . DGEList calcNormFactors colData counts design end estimate
      estimateSizeFactors exprs<- fData<- gene gr is lambda model.matrix
      p.adjust pData pData<- pi0 protein rowRanges sample.id seqnames
      setNames smoothed start tbl_dt term value voom voomWithQualityWeights
    Consider adding
      importFrom("methods", "is")
      importFrom("stats", "end", "model.matrix", "p.adjust", "setNames",
                 "start")
    to your NAMESPACE file (and ensure that your DESCRIPTION Imports field
    contains 'methods').
    ```

## Newly fixed

*   checking whether package ‘biobroom’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/biobroom/old/biobroom.Rcheck/00install.out’ for details.
    ```

# breathteststan

Version: 0.3.0

## Newly broken

*   checking installed package size ... NOTE
    ```
      installed size is 24.7Mb
      sub-directories of 1Mb or more:
        libs  24.5Mb
    ```

## Newly fixed

*   checking whether package ‘breathteststan’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/breathteststan/old/breathteststan.Rcheck/00install.out’ for details.
    ```

# broom

Version: 0.4.2

## Newly broken

*   checking examples ... ERROR
    ```
    ...
    +   f2 <- Finance[1:300, "hml"] - rf
    +   f3 <- Finance[1:300, "smb"] - rf
    +   h <- cbind(f1, f2, f3)
    +   res2 <- gmm(z ~ f1 + f2 + f3, x = h)
    +   
    +   td2 <- tidy(res2, conf.int = TRUE)
    +   td2
    +   
    +   # coefficient plot
    +   td2 %>%
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
    ```

## Newly fixed

*   checking whether package ‘broom’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/broom/old/broom.Rcheck/00install.out’ for details.
    ```

# cdata

Version: 0.1.5

## Newly broken

*   checking examples ... ERROR
    ```
    Running examples in ‘cdata-Ex.R’ failed
    The error most likely occurred in:
    
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
    ```

## Newly fixed

*   checking whether package ‘cdata’ can be installed ... WARNING
    ```
    Found the following significant warnings:
      Warning: Installed Rcpp (0.12.12) different from Rcpp used to build dplyr (0.12.11).
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/cdata/old/cdata.Rcheck/00install.out’ for details.
    ```

## In both

*   checking re-building of vignette outputs ... WARNING
    ```
    Error in re-building vignettes:
      ...
    Quitting from lines 284-292 (RowsAndColumns.Rmd) 
    Error: processing vignette 'RowsAndColumns.Rmd' failed with diagnostics:
    Variable context not set
    Execution halted
    ```

# congressbr

Version: 0.1.1

## Newly broken

*   checking data for non-ASCII characters ... NOTE
    ```
      Note: found 1 marked UTF-8 string
    ```

## Newly fixed

*   checking whether package ‘congressbr’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/congressbr/old/congressbr.Rcheck/00install.out’ for details.
    ```

# countyfloods

Version: 0.0.2

## Newly broken

*   R CMD check timed out
    ```
    ```

## Newly fixed

*   checking examples ... ERROR
    ```
    Running examples in ‘countyfloods-Ex.R’ failed
    The error most likely occurred in:
    
    > ### Name: find_nws
    > ### Title: Get National Weather Service (NWS) flood stage/discharge levels
    > ###   for gages.
    > ### Aliases: find_nws
    > 
    > ### ** Examples
    > 
    > 
    > va_counties <- get_county_cd("Virginia")
    > va_gages <- get_gages(va_counties, start_date = "2015-01-01",
    +                       end_date = "2015-12-31")
    Error in dyn.load(file, DLLpath = DLLpath, ...) : 
      unable to load shared object '/home/muelleki/git/R/tidyr/revdep/library/tidyr/old/stringi/libs/stringi.so':
      libicui18n.so.57: cannot open shared object file: No such file or directory
    Calls: get_gages ... tryCatch -> tryCatchList -> tryCatchOne -> <Anonymous>
    Execution halted
    ```

*   checking whether package ‘countyfloods’ can be installed ... WARNING
    ```
    Found the following significant warnings:
      Warning: Installed Rcpp (0.12.12) different from Rcpp used to build dplyr (0.12.11).
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/countyfloods/old/countyfloods.Rcheck/00install.out’ for details.
    ```

*   checking re-building of vignette outputs ... WARNING
    ```
    Error in re-building vignettes:
      ...
    Error: processing vignette 'countyflood.Rmd' failed with diagnostics:
    unable to load shared object '/home/muelleki/git/R/tidyr/revdep/library/tidyr/old/stringi/libs/stringi.so':
      libicui18n.so.57: cannot open shared object file: No such file or directory
    Execution halted
    ```

# curatedMetagenomicData

Version: 1.2.0

## Newly broken

*   checking installed package size ... NOTE
    ```
      installed size is  8.6Mb
      sub-directories of 1Mb or more:
        help   7.9Mb
    ```

*   checking DESCRIPTION meta-information ... NOTE
    ```
    Package listed in more than one of Depends, Imports, Suggests, Enhances:
      ‘BiocInstaller’
    A package should be listed in only one of these fields.
    ```

*   checking dependencies in R code ... NOTE
    ```
    Namespace in Imports field not imported from: ‘BiocInstaller’
      All declared Imports should be used.
    ```

*   checking R code for possible problems ... NOTE
    ```
    ExpressionSet2MRexperiment: no visible global function definition for
      ‘AnnotatedDataFrame’
    ExpressionSet2MRexperiment: no visible global function definition for
      ‘phenoData’
    curatedMetagenomicData : <anonymous>: no visible global function
      definition for ‘exprs<-’
    Undefined global functions or variables:
      AnnotatedDataFrame exprs<- phenoData
    ```

*   checking Rd files ... NOTE
    ```
    prepare_Rd: HMP_2012.Rd:540-542: Dropping empty section \seealso
    prepare_Rd: KarlssonFH_2013.Rd:90-92: Dropping empty section \seealso
    prepare_Rd: LeChatelierE_2013.Rd:86-88: Dropping empty section \seealso
    prepare_Rd: LomanNJ_2013_Hi.Rd:82-84: Dropping empty section \seealso
    prepare_Rd: LomanNJ_2013_Mi.Rd:82-84: Dropping empty section \seealso
    prepare_Rd: NielsenHB_2014.Rd:94-96: Dropping empty section \seealso
    prepare_Rd: Obregon_TitoAJ_2015.Rd:94-96: Dropping empty section \seealso
    prepare_Rd: OhJ_2014.Rd:86-88: Dropping empty section \seealso
    prepare_Rd: QinJ_2012.Rd:106-108: Dropping empty section \seealso
    prepare_Rd: QinN_2014.Rd:94-96: Dropping empty section \seealso
    prepare_Rd: RampelliS_2015.Rd:90-92: Dropping empty section \seealso
    prepare_Rd: TettAJ_2016.Rd:184-186: Dropping empty section \seealso
    prepare_Rd: ZellerG_2014.Rd:94-96: Dropping empty section \seealso
    ```

## Newly fixed

*   checking whether package ‘curatedMetagenomicData’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/curatedMetagenomicData/old/curatedMetagenomicData.Rcheck/00install.out’ for details.
    ```

## In both

*   checking package dependencies ... NOTE
    ```
    Depends: includes the non-default packages:
      ‘dplyr’ ‘phyloseq’ ‘Biobase’ ‘ExperimentHub’ ‘AnnotationHub’
      ‘magrittr’
    Adding so many packages to the search path is excessive and importing
    selectively is preferable.
    ```

# d3r

Version: 0.6.6

## Newly broken

*   checking examples ... ERROR
    ```
    ...
    > library(dplyr)
    
    Attaching package: ‘dplyr’
    
    The following objects are masked from ‘package:stats’:
    
        filter, lag
    
    The following objects are masked from ‘package:base’:
    
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
    ```

## In both

*   checking package dependencies ... NOTE
    ```
    Packages which this enhances but not available for checking:
      ‘igraph’ ‘partykit’ ‘treemap’ ‘V8’
    ```

# DChIPRep

Version: 1.6.1

## Newly broken

*   checking DESCRIPTION meta-information ... NOTE
    ```
    Malformed Description field: should contain one or more complete sentences.
    ```

## Newly fixed

*   checking whether package ‘DChIPRep’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/DChIPRep/old/DChIPRep.Rcheck/00install.out’ for details.
    ```

# DeepBlueR

Version: 1.2.6

## Newly broken

*   checking examples ... ERROR
    ```
    ...
    > data_id = deepblue_select_experiments(
    +     experiment_name="E002-H3K9ac.narrowPeak.bed")
    Called method: deepblue_select_experiments
    Reported status was: okay
    > 
    > filtered_id = deepblue_filter_regions(query_id = data_id,
    +     field = "VALUE",
    +     operation = ">",
    +     value = "100",
    +     type = "number",
    +     user_key = "anonymous_key")
    Called method: deepblue_filter_regions
    Reported status was: okay
    > 
    > deepblue_calculate_enrichment(query_id = filtered_id,
    +    gene_model = "gencode v23")
    Called method: deepblue_calculate_enrichment
    Reported status was: error
    Error in deepblue_calculate_enrichment(query_id = filtered_id, gene_model = "gencode v23") : 
      Command calculate_enrichment does not exists.
    Execution halted
    ```

## Newly fixed

*   checking whether package ‘DeepBlueR’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/DeepBlueR/old/DeepBlueR.Rcheck/00install.out’ for details.
    ```

# ENCODExplorer

Version: 2.2.0

## Newly broken

*   checking installed package size ... NOTE
    ```
      installed size is 73.6Mb
      sub-directories of 1Mb or more:
        data     23.9Mb
        doc       1.5Mb
        extdata  48.0Mb
    ```

*   checking R code for possible problems ... NOTE
    ```
    ...
      ‘biosample_type’
    step6_control: no visible binding for global variable ‘controls’
    step6_date_released: no visible binding for global variable
      ‘date_released’
    step6_status: no visible binding for global variable ‘status’
    step6_target: no visible binding for global variable ‘target’
    step7: no visible binding for global variable ‘organism’
    step8: no visible binding for global variable ‘investigated_as’
    step8: no visible binding for global variable ‘target’
    step9: no visible binding for global variable ‘organism’
    Undefined global functions or variables:
      . Experiment Value accession antibody_caption
      antibody_characterization antibody_target assay
      biological_replicate_number biosample_name biosample_type col_name
      controls data date_released download.file encode_df file_accession
      file_format href investigated_as lab nucleic_acid_term organism
      platform project replicate_antibody replicate_library server status
      submitted_by target technical_replicate_number treatment ui value
    Consider adding
      importFrom("utils", "data", "download.file")
    to your NAMESPACE file.
    ```

*   checking data for non-ASCII characters ... NOTE
    ```
      Note: found 771 marked UTF-8 strings
    ```

## Newly fixed

*   checking whether package ‘ENCODExplorer’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/ENCODExplorer/old/ENCODExplorer.Rcheck/00install.out’ for details.
    ```

# eurostat

Version: 3.1.1

## Newly broken

*   checking re-building of vignette outputs ... WARNING
    ```
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

## Newly fixed

*   checking whether package ‘eurostat’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/eurostat/old/eurostat.Rcheck/00install.out’ for details.
    ```

# eyetrackingR

Version: 0.1.6

## Newly broken

*   R CMD check timed out
    ```
    ```

## Newly fixed

*   checking whether package ‘eyetrackingR’ can be installed ... WARNING
    ```
    Found the following significant warnings:
      Warning: Installed Rcpp (0.12.12) different from Rcpp used to build dplyr (0.12.11).
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/eyetrackingR/old/eyetrackingR.Rcheck/00install.out’ for details.
    ```

*   checking re-building of vignette outputs ... WARNING
    ```
    Error in re-building vignettes:
      ...
    Error: processing vignette 'divergence_vignette.Rmd' failed with diagnostics:
    unable to load shared object '/home/muelleki/git/R/tidyr/revdep/library/tidyr/old/stringi/libs/stringi.so':
      libicui18n.so.57: cannot open shared object file: No such file or directory
    Execution halted
    ```

## In both

*   checking examples ... ERROR
    ```
    ...
    +                                time_column = "TimeFromTrialOnset",
    +                                trackloss_column = "TrackLoss",
    +                                aoi_columns = c('Animate','Inanimate'),
    +                                treat_non_aoi_looks_as_missing = TRUE )
    `mutate_each()` is deprecated.
    Use `mutate_all()`, `mutate_at()` or `mutate_if()` instead.
    To map `funs` over a selection of variables, use `mutate_at()`
    > response_window <- subset_by_window(data, window_start_time = 15500, window_end_time = 21000, 
    +                                     rezero = FALSE)
    Avg. window length in new data will be 5500
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
    ```

# fbar

Version: 0.1.23

## Newly broken

*   checking re-building of vignette outputs ... WARNING
    ```
    Error in re-building vignettes:
      ...
    
    Attaching package: 'dplyr'
    
    The following objects are masked from 'package:stats':
    
        filter, lag
    
    The following objects are masked from 'package:base':
    
        intersect, setdiff, setequal, union
    
    ROI.plugin.glpk: R Optimization Infrastructure
    Registered solver plugins: nlminb, ecos, glpk.
    Default solver: auto.
    Quitting from lines 19-22 (Multi-Objective_Optimization_case_study.Rmd) 
    Error: processing vignette 'Multi-Objective_Optimization_case_study.Rmd' failed with diagnostics:
    there is no package called 'tidyverse'
    Execution halted
    ```

## Newly fixed

*   checking whether package ‘fbar’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/fbar/old/fbar.Rcheck/00install.out’ for details.
    ```

## In both

*   checking package dependencies ... NOTE
    ```
    Package suggested but not available for checking: ‘tidyverse’
    ```

# flextable

Version: 0.2.0

## Newly broken

*   checking re-building of vignette outputs ... WARNING
    ```
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

## Newly fixed

*   checking whether package ‘flextable’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/flextable/old/flextable.Rcheck/00install.out’ for details.
    ```

# geoparser

Version: 0.1.1

## Newly broken

*   checking re-building of vignette outputs ... WARNING
    ```
    Error in re-building vignettes:
      ...
    Quitting from lines 34-37 (geoparser.Rmd) 
    Error: processing vignette 'geoparser.Rmd' failed with diagnostics:
    HTTP failure: 401
    Execution halted
    ```

## Newly fixed

*   checking whether package ‘geoparser’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/geoparser/old/geoparser.Rcheck/00install.out’ for details.
    ```

# hansard

Version: 0.5.0

## Newly broken

*   R CMD check timed out
    ```
    ```

## Newly fixed

*   checking whether package ‘hansard’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/hansard/old/hansard.Rcheck/00install.out’ for details.
    ```

# highcharter

Version: 0.5.0

## Newly broken

*   checking installed package size ... NOTE
    ```
      installed size is 16.5Mb
      sub-directories of 1Mb or more:
        doc          13.7Mb
        htmlwidgets   1.9Mb
    ```

## Newly fixed

*   checking whether package ‘highcharter’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/highcharter/old/highcharter.Rcheck/00install.out’ for details.
    ```

# IHWpaper

Version: 1.4.0

## Newly broken

*   checking installed package size ... NOTE
    ```
      installed size is 14.9Mb
      sub-directories of 1Mb or more:
        doc       3.4Mb
        extdata   9.8Mb
    ```

*   checking R code for possible problems ... NOTE
    ```
    scott_fdrreg: no visible global function definition for ‘FDRreg’
    scott_fdrreg: no visible global function definition for ‘getFDR’
    sim_fun_eval: no visible binding for global variable ‘fdr_method’
    sim_fun_eval: no visible binding for global variable ‘fdr_pars’
    sim_fun_eval: no visible binding for global variable ‘FDP’
    sim_fun_eval: no visible binding for global variable ‘rj_ratio’
    sim_fun_eval: no visible binding for global variable ‘FPR’
    sim_fun_eval: no visible binding for global variable ‘FWER’
    Undefined global functions or variables:
      FDP FDRreg FPR FWER fdr_method fdr_pars getFDR rj_ratio
    ```

## Newly fixed

*   checking whether package ‘IHWpaper’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/IHWpaper/old/IHWpaper.Rcheck/00install.out’ for details.
    ```

# IONiseR

Version: 2.0.0

## Newly broken

*   checking installed package size ... NOTE
    ```
      installed size is  5.4Mb
      sub-directories of 1Mb or more:
        doc       3.6Mb
        extdata   1.5Mb
    ```

*   checking R code for possible problems ... NOTE
    ```
    ...
      ‘start_time’
    readFast5Summary.mc: no visible binding for global variable ‘duration’
    readFast5Summary.mc: no visible binding for global variable
      ‘num_events’
    [,Fast5Summary-ANY-ANY-ANY: no visible binding for global variable
      ‘baseCalledTemplate’
    [,Fast5Summary-ANY-ANY-ANY: no visible binding for global variable
      ‘baseCalledComplement’
    [,Fast5Summary-ANY-ANY-ANY: no visible binding for global variable
      ‘component’
    [,Fast5Summary-ANY-ANY-ANY: no visible binding for global variable
      ‘idx’
    show,Fast5Summary: no visible binding for global variable ‘full_2D’
    show,Fast5Summary: no visible binding for global variable ‘pass’
    Undefined global functions or variables:
      := AAAAA TTTTT accumulation baseCalledComplement baseCalledTemplate
      bases_called category channel circleFun component duration error freq
      full_2D group hour idx matrixCol matrixRow meanZValue mean_value
      median_signal minute mux name nbases new_reads num_events oddEven
      pass pentamer rbindlist readIDs seq_length start_time time_bin
      time_group x y zvalue
    ```

## Newly fixed

*   checking whether package ‘IONiseR’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/IONiseR/old/IONiseR.Rcheck/00install.out’ for details.
    ```

# isomiRs

Version: 1.4.0

## Newly broken

*   checking examples ... ERROR
    ```
    Running examples in ‘isomiRs-Ex.R’ failed
    The error most likely occurred in:
    
    > ### Name: isoNetwork
    > ### Title: Clustering miRNAs-genes pairs in similar pattern expression
    > ### Aliases: isoNetwork
    > 
    > ### ** Examples
    > 
    > 
    > library(org.Mm.eg.db)
    Loading required package: AnnotationDbi
    
    > library(clusterProfiler)
    Error in library(clusterProfiler) : 
      there is no package called ‘clusterProfiler’
    Execution halted
    ```

*   checking R code for possible problems ... NOTE
    ```
    ...
    isoSelect.IsomirDataSeq: no visible binding for global variable ‘freq’
    isoSelect,IsomirDataSeq : <anonymous>: no visible binding for global
      variable ‘mir’
    isoSelect,IsomirDataSeq : <anonymous>: no visible binding for global
      variable ‘mism’
    isoSelect,IsomirDataSeq : <anonymous>: no visible binding for global
      variable ‘add’
    isoSelect,IsomirDataSeq : <anonymous>: no visible binding for global
      variable ‘t5’
    isoSelect,IsomirDataSeq : <anonymous>: no visible binding for global
      variable ‘t3’
    isoSelect,IsomirDataSeq : <anonymous>: no visible binding for global
      variable ‘id’
    isoSelect,IsomirDataSeq : <anonymous>: no visible binding for global
      variable ‘freq’
    isoSelect,IsomirDataSeq: no visible binding for global variable ‘freq’
    Undefined global functions or variables:
      Count DB X1 X2 add af ambiguity average change condition current
      enrich enrichGO error freq gene go group id mir mir_f mir_n mism
      mism_f mism_n ngene pct_abundance reference rowMax rowMin sel_genes
      t3 t5 term term_short type value y
    ```

## Newly fixed

*   checking whether package ‘isomiRs’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/isomiRs/old/isomiRs.Rcheck/00install.out’ for details.
    ```

## In both

*   checking package dependencies ... NOTE
    ```
    Package suggested but not available for checking: ‘clusterProfiler’
    ```

# jpmesh

Version: 0.3.0

## Newly broken

*   checking installed package size ... NOTE
    ```
      installed size is 206.0Mb
      sub-directories of 1Mb or more:
        extdata  205.2Mb
    ```

## Newly fixed

*   checking whether package ‘jpmesh’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/jpmesh/old/jpmesh.Rcheck/00install.out’ for details.
    ```

# lans2r

Version: 1.0.5

## Newly broken

*   checking re-building of vignette outputs ... WARNING
    ```
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

## Newly fixed

*   checking whether package ‘lans2r’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/lans2r/old/lans2r.Rcheck/00install.out’ for details.
    ```

# mafs

Version: 0.0.2

## Newly broken

*   checking examples ... ERROR
    ```
    Running examples in ‘mafs-Ex.R’ failed
    The error most likely occurred in:
    
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

## In both

*   checking dependencies in R code ... NOTE
    ```
    Namespaces in Imports field not imported from:
      ‘Rcpp’ ‘cmprsk’ ‘colorspace’ ‘etm’ ‘fracdiff’ ‘gtable’ ‘munsell’
      ‘numDeriv’ ‘plyr’ ‘quadprog’ ‘scales’ ‘timeDate’ ‘tseries’ ‘zoo’
      All declared Imports should be used.
    ```

# MANOVA.RM

Version: 0.1.1

## Newly broken

*   checking re-building of vignette outputs ... WARNING
    ```
    ...
    11: timing_fn(handle(ev <- withCallingHandlers(withVisible(eval(expr,     envir, enclos)), warning = wHandler, error = eHandler, message = mHandler)))
    12: evaluate_call(expr, parsed$src[[i]], envir = envir, enclos = enclos,     debug = debug, last = i == length(out), use_try = stop_on_error !=         2L, keep_warning = keep_warning, keep_message = keep_message,     output_handler = output_handler, include_timing = include_timing)
    13: evaluate(code, envir = env, new_device = FALSE, keep_warning = !isFALSE(options$warning),     keep_message = !isFALSE(options$message), stop_on_error = if (options$error &&         options$include) 0L else 2L, output_handler = knit_handlers(options$render,         options))
    14: in_dir(input_dir(), evaluate(code, envir = env, new_device = FALSE,     keep_warning = !isFALSE(options$warning), keep_message = !isFALSE(options$message),     stop_on_error = if (options$error && options$include) 0L else 2L,     output_handler = knit_handlers(options$render, options)))
    15: block_exec(params)
    16: call_block(x)
    17: process_group.block(group)
    18: process_group(group)
    19: withCallingHandlers(if (tangle) process_tangle(group) else process_group(group),     error = function(e) {        setwd(wd)        cat(res, sep = "\n", file = output %n% "")        message("Quitting from lines ", paste(current_lines(i),             collapse = "-"), " (", knit_concord$get("infile"),             ") ")    })
    20: process_file(text, output)
    21: knitr::knit(knit_input, knit_output, envir = envir, quiet = quiet,     encoding = encoding)
    22: rmarkdown::render(file, encoding = encoding, quiet = quiet, envir = globalenv())
    23: vweave_rmarkdown(...)
    24: engine$weave(file, quiet = quiet, encoding = enc)
    25: doTryCatch(return(expr), name, parentenv, handler)
    26: tryCatchOne(expr, names, parentenv, handlers[[1L]])
    27: tryCatchList(expr, classes, parentenv, handlers)
    28: tryCatch({    engine$weave(file, quiet = quiet, encoding = enc)    setwd(startdir)    find_vignette_product(name, by = "weave", engine = engine)}, error = function(e) {    stop(gettextf("processing vignette '%s' failed with diagnostics:\n%s",         file, conditionMessage(e)), domain = NA, call. = FALSE)})
    29: buildVignettes(dir = "/home/muelleki/git/R/tidyr/revdep/checks/MANOVA.RM/new/MANOVA.RM.Rcheck/vign_test/MANOVA.RM")
    An irrecoverable exception occurred. R is aborting now ...
    Segmentation fault (core dumped)
    ```

## Newly fixed

*   checking re-building of vignette outputs ... NOTE
    ```
    Error in re-building vignettes:
      ...
    Error in loadVignetteBuilder(vigns$pkgdir) : 
      vignette builder 'rmarkdown' not found
    Calls: buildVignettes -> loadVignetteBuilder
    Execution halted
    ```

## In both

*   checking Rd cross-references ... NOTE
    ```
    Package unavailable to check Rd xrefs: ‘nparLD’
    ```

# mtconnectR

Version: 1.1.0

## Newly broken

*   checking examples ... ERROR
    ```
    ...
    The error most likely occurred in:
    
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
    ```

*   checking re-building of vignette outputs ... WARNING
    ```
    Error in re-building vignettes:
      ...
    Quitting from lines 102-107 (simulate_map_gcode.Rmd) 
    Error: processing vignette 'simulate_map_gcode.Rmd' failed with diagnostics:
    Variable context not set
    Execution halted
    ```

## Newly fixed

*   checking whether package ‘mtconnectR’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/mtconnectR/old/mtconnectR.Rcheck/00install.out’ for details.
    ```

# MultiAssayExperiment

Version: 1.2.1

## Newly broken

*   checking examples ... WARNING
    ```
    ...
      Warning: 'RangedRaggedAssay' is deprecated.
      Warning: 'RangedRaggedAssay' is deprecated.
      Warning: 'RangedRaggedAssay' is deprecated.
      Warning: 'RangedRaggedAssay' is deprecated.
      Warning: 'RangedRaggedAssay' is deprecated.
      Warning: 'RangedRaggedAssay' is deprecated.
      Warning: 'RangedRaggedAssay' is deprecated.
      Warning: 'RangedRaggedAssay' is deprecated.
      Warning: 'RangedRaggedAssay' is deprecated.
      Warning: 'RangedRaggedAssay' is deprecated.
      Warning: 'RangedRaggedAssay' is deprecated.
      Warning: 'RangedRaggedAssay' is deprecated.
      Warning: 'RangedRaggedAssay' is deprecated.
      Warning: 'RangedRaggedAssay' is deprecated.
      Warning: 'RangedRaggedAssay' is deprecated.
      Warning: 'RangedRaggedAssay' is deprecated.
      Warning: 'RangedRaggedAssay' is deprecated.
      Warning: 'RangedRaggedAssay' is deprecated.
    Deprecated functions may be defunct as soon as of the next release of
    R.
    See ?Deprecated.
    ```

*   checking dependencies in R code ... NOTE
    ```
    Unexported object imported by a ':::' call: ‘BiocGenerics:::replaceSlots’
      See the note in ?`:::` about the use of this operator.
    ```

## Newly fixed

*   checking whether package ‘MultiAssayExperiment’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/MultiAssayExperiment/old/MultiAssayExperiment.Rcheck/00install.out’ for details.
    ```

# NFP

Version: 0.99.2

## Newly broken

*   checking installed package size ... NOTE
    ```
      installed size is  8.1Mb
      sub-directories of 1Mb or more:
        data   7.5Mb
    ```

## Newly fixed

*   checking whether package ‘NFP’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/NFP/old/NFP.Rcheck/00install.out’ for details.
    ```

## In both

*   checking package dependencies ... NOTE
    ```
    Package suggested but not available for checking: ‘NFPdata’
    ```

# nzelect

Version: 0.3.3

## Newly broken

*   R CMD check timed out
    ```
    ```

## Newly fixed

*   checking re-building of vignette outputs ... WARNING
    ```
    Error in re-building vignettes:
      ...
    Error: processing vignette 'README.Rmd' failed with diagnostics:
    unable to load shared object '/home/muelleki/git/R/tidyr/revdep/library/tidyr/old/stringi/libs/stringi.so':
      libicui18n.so.57: cannot open shared object file: No such file or directory
    Execution halted
    ```

## In both

*   checking data for non-ASCII characters ... NOTE
    ```
      Note: found 4204 marked UTF-8 strings
    ```

# parsemsf

Version: 0.1.0

## Newly broken

*   checking examples ... ERROR
    ```
    Running examples in ‘parsemsf-Ex.R’ failed
    The error most likely occurred in:
    
    > ### Name: make_area_table
    > ### Title: Make a table of peptide areas
    > ### Aliases: make_area_table
    > 
    > ### ** Examples
    > 
    > make_area_table(parsemsf_example("test_db.msf"))
    Error: The dbplyr package is required to communicate with database backends.
    Execution halted
    ```

*   checking re-building of vignette outputs ... WARNING
    ```
    Error in re-building vignettes:
      ...
    Quitting from lines 20-25 (introduction.Rmd) 
    Error: processing vignette 'introduction.Rmd' failed with diagnostics:
    The dbplyr package is required to communicate with database backends.
    Execution halted
    ```

*   checking dependencies in R code ... NOTE
    ```
    Namespace in Imports field not imported from: ‘RSQLite’
      All declared Imports should be used.
    ```

## Newly fixed

*   checking whether package ‘parsemsf’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/parsemsf/old/parsemsf.Rcheck/00install.out’ for details.
    ```

# proteoQC

Version: 1.12.3

## Newly broken

*   checking re-building of vignette outputs ... WARNING
    ```
    Error in re-building vignettes:
      ...
    Error: processing vignette 'proteoQC.Rmd' failed with diagnostics:
    there is no package called ‘prettydoc’
    Execution halted
    ```

*   checking installed package size ... NOTE
    ```
      installed size is  8.0Mb
      sub-directories of 1Mb or more:
        doc       3.2Mb
        extdata   4.0Mb
    ```

*   checking R code for possible problems ... NOTE
    ```
    ...
    plotMS2boxplot: no visible binding for global variable ‘techRep’
    plotMS2boxplot: no visible binding for global variable ‘fraction’
    plotMS2boxplot: no visible binding for global variable ‘MS2QC’
    plotSampleIDResultErrorBar: no visible binding for global variable
      ‘fraction’
    plotSampleIDResultErrorBar: no visible binding for global variable
      ‘val’
    plotSampleIDResultErrorBar: no visible binding for global variable ‘se’
    plotSampleVenn: no visible global function definition for ‘grid.draw’
    plotTechRepVenn : <anonymous>: no visible global function definition
      for ‘grid.draw’
    qcHist: no visible binding for global variable ‘error’
    qcHist: no visible binding for global variable ‘techRep’
    qcHist: no visible binding for global variable ‘bioRep’
    qcHist2: no visible binding for global variable ‘error’
    qcHist2: no visible binding for global variable ‘fractile’
    Undefined global functions or variables:
      ..count.. Intensity MS1QC MS2QC TMT10 TMT6 Tag V1 V2 V3 V4 V5 bioRep
      curenv delta error exprs fractile fraction grid.draw iTRAQ4 iTRAQ8
      label peplength peptide_summary precursorCharge quantify ratio
      readMgfData se techRep val x y
    ```

## Newly fixed

*   checking whether package ‘proteoQC’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/proteoQC/old/proteoQC.Rcheck/00install.out’ for details.
    ```

## In both

*   checking package dependencies ... NOTE
    ```
    Package suggested but not available for checking: ‘RforProteomics’
    ```

# qdap

Version: 2.2.5

## Newly broken

*   checking Rd cross-references ... NOTE
    ```
    Package unavailable to check Rd xrefs: ‘gplots’
    ```

## Newly fixed

*   checking whether package ‘qdap’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/qdap/old/qdap.Rcheck/00install.out’ for details.
    ```

# rprev

Version: 0.2.3

## Newly broken

*   R CMD check timed out
    ```
    ```

## Newly fixed

*   checking whether package ‘rprev’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/rprev/old/rprev.Rcheck/00install.out’ for details.
    ```

# sejmRP

Version: 1.3.4

## Newly broken

*   checking dependencies in R code ... NOTE
    ```
    Namespaces in Imports field not imported from:
      ‘cluster’ ‘factoextra’ ‘tidyr’
      All declared Imports should be used.
    ```

## Newly fixed

*   checking whether package ‘sejmRP’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/sejmRP/old/sejmRP.Rcheck/00install.out’ for details.
    ```

# shazam

Version: 0.1.8

## Newly broken

*   checking re-building of vignette outputs ... WARNING
    ```
    Error in re-building vignettes:
      ...
    Loading required package: ggplot2
    Quitting from lines 282-285 (Baseline-Vignette.Rmd) 
    Error: processing vignette 'Baseline-Vignette.Rmd' failed with diagnostics:
    `-0.98`, `-0.969999999999999`, `-0.960000000000001`, `-0.949999999999999`, `-0.940000000000001`, ... must resolve to integer column positions, not a double vector
    Execution halted
    ```

*   checking data for non-ASCII characters ... NOTE
    ```
      Note: found 2 marked UTF-8 strings
    ```

## Newly fixed

*   checking whether package ‘shazam’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/shazam/old/shazam.Rcheck/00install.out’ for details.
    ```

# sjmisc

Version: 2.5.0

## Newly broken

*   checking examples ... ERROR
    ```
    ...
    +   group_by(e42dep) %>%
    +   nest() %>%
    +   mutate(
    +     models = map(data, ~lm(neg_c_7 ~ c12hour + c172code, data = .x))
    +   ) %>%
    +   spread_coef(models)
    # A tibble: 4 x 6
      e42dep                data   models `(Intercept)`     c12hour    c172code
       <dbl>              <list>   <list>         <dbl>       <dbl>       <dbl>
    1      3 <tibble [306 x 25]> <S3: lm>      10.89687 0.003720769  0.38545070
    2      4 <tibble [304 x 25]> <S3: lm>      12.96112 0.008242511  0.04913521
    3      1  <tibble [66 x 25]> <S3: lm>      10.92300 0.012767707 -1.00230234
    4      2 <tibble [225 x 25]> <S3: lm>       8.27386 0.034491212  0.77048799
    > 
    > # spread_coef() makes it easy to generate bootstrapped
    > # confidence intervals, using the 'bootstrap()' and 'boot_ci()'
    > # functions from the 'sjstats' package, which creates nested
    > # data frames of bootstrap replicates
    > library(sjstats)
    Error in library(sjstats) : there is no package called ‘sjstats’
    Execution halted
    ```

*   checking Rd cross-references ... NOTE
    ```
    Package unavailable to check Rd xrefs: ‘sjstats’
    ```

## Newly fixed

*   checking whether package ‘sjmisc’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/sjmisc/old/sjmisc.Rcheck/00install.out’ for details.
    ```

## In both

*   checking package dependencies ... NOTE
    ```
    Packages suggested but not available for checking: ‘sjPlot’ ‘sjstats’
    ```

# starmie

Version: 0.1.2

## Newly broken

*   checking installed package size ... NOTE
    ```
      installed size is  7.0Mb
      sub-directories of 1Mb or more:
        doc       1.1Mb
        extdata   4.9Mb
    ```

*   checking dependencies in R code ... NOTE
    ```
    Namespace in Imports field not imported from: ‘MCMCpack’
      All declared Imports should be used.
    ```

## Newly fixed

*   checking whether package ‘starmie’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/starmie/old/starmie.Rcheck/00install.out’ for details.
    ```

# subSeq

Version: 1.6.0

## Newly broken

*   checking R code for possible problems ... NOTE
    ```
    ...
    summary.subsamples: no visible binding for global variable ‘o.padj’
    summary.subsamples: no visible binding for global variable
      ‘significant’
    summary.subsamples: no visible binding for global variable ‘estFDP’
    summary.subsamples: no visible binding for global variable ‘rFDP’
    summary.subsamples: no visible binding for global variable ‘metric’
    summary.subsamples: no visible binding for global variable ‘value’
    summary.subsamples: no visible binding for global variable ‘percent’
    voomLimma: no visible global function definition for ‘model.matrix’
    Undefined global functions or variables:
      . ID average.depth average.value coefficient cor count cov depth
      estFDP method metric model.matrix o.coefficient o.lfdr o.padj
      p.adjust padj percent plot proportion pvalue rFDP rbinom replication
      selectMethod significant valid value var
    Consider adding
      importFrom("graphics", "plot")
      importFrom("methods", "selectMethod")
      importFrom("stats", "cor", "cov", "model.matrix", "p.adjust", "rbinom",
                 "var")
    to your NAMESPACE file (and ensure that your DESCRIPTION Imports field
    contains 'methods').
    ```

## Newly fixed

*   checking whether package ‘subSeq’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/subSeq/old/subSeq.Rcheck/00install.out’ for details.
    ```

# survminer

Version: 0.4.0

## Newly broken

*   checking installed package size ... NOTE
    ```
      installed size is  5.6Mb
      sub-directories of 1Mb or more:
        doc   5.3Mb
    ```

## Newly fixed

*   checking whether package ‘survminer’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/survminer/old/survminer.Rcheck/00install.out’ for details.
    ```

# textreuse

Version: 0.1.4

## Newly broken

*   checking examples ... ERROR
    ```
    Running examples in ‘textreuse-Ex.R’ failed
    The error most likely occurred in:
    
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
    ```

*   checking Rd cross-references ... NOTE
    ```
    Package unavailable to check Rd xrefs: ‘tm’
    ```

## Newly fixed

*   checking whether package ‘textreuse’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/textreuse/old/textreuse.Rcheck/00install.out’ for details.
    ```

# tidygenomics

Version: 0.1.0

## Newly broken

*   checking examples ... ERROR
    ```
    ...
    
    Attaching package: ‘dplyr’
    
    The following objects are masked from ‘package:stats’:
    
        filter, lag
    
    The following objects are masked from ‘package:base’:
    
        intersect, setdiff, setequal, union
    
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
    ```

## Newly fixed

*   checking whether package ‘tidygenomics’ can be installed ... WARNING
    ```
    Found the following significant warnings:
      Warning: Installed Rcpp (0.12.12) different from Rcpp used to build dplyr (0.12.11).
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/tidygenomics/old/tidygenomics.Rcheck/00install.out’ for details.
    ```

## In both

*   checking re-building of vignette outputs ... WARNING
    ```
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

# translateSPSS2R

Version: 1.0.0

## Newly broken

*   checking R code for possible problems ... NOTE
    ```
    ...
    xpssMeans: no visible global function definition for ‘anova’
    xpssRegression: no visible global function definition for ‘na.omit’
    xpssRegression: no visible global function definition for ‘anova’
    xpssRegression: no visible binding for global variable ‘sd’
    xpssTtest: no visible global function definition for ‘complete.cases’
    xpssTtest: no visible global function definition for ‘t.test’
    xpssTtest: no visible global function definition for ‘na.omit’
    xpssTtest: no visible global function definition for ‘sd’
    xpssTtest: no visible global function definition for ‘var’
    xpssTtest: no visible global function definition for ‘cor.test’
    Undefined global functions or variables:
      anova as.formula complete.cases cor.test density frequency
      globalVariables head lines lm median na.omit quantile sd summary.lm
      t.test tail title var
    Consider adding
      importFrom("graphics", "lines", "title")
      importFrom("stats", "anova", "as.formula", "complete.cases",
                 "cor.test", "density", "frequency", "lm", "median",
                 "na.omit", "quantile", "sd", "summary.lm", "t.test", "var")
      importFrom("utils", "globalVariables", "head", "tail")
    to your NAMESPACE file.
    ```

## Newly fixed

*   checking whether package ‘translateSPSS2R’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/translateSPSS2R/old/translateSPSS2R.Rcheck/00install.out’ for details.
    ```

# valr

Version: 0.3.0

## Newly broken

*   checking installed package size ... NOTE
    ```
      installed size is 16.4Mb
      sub-directories of 1Mb or more:
        libs  14.8Mb
    ```

## Newly fixed

*   checking whether package ‘valr’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/valr/old/valr.Rcheck/00install.out’ for details.
    ```

# WRTDStidal

Version: 1.1.0

## Newly broken

*   checking examples ... ERROR
    ```
    Running examples in ‘WRTDStidal-Ex.R’ failed
    The error most likely occurred in:
    
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

## Newly fixed

*   checking whether package ‘WRTDStidal’ can be installed ... ERROR
    ```
    Installation failed.
    See ‘/home/muelleki/git/R/tidyr/revdep/checks/WRTDStidal/old/WRTDStidal.Rcheck/00install.out’ for details.
    ```

