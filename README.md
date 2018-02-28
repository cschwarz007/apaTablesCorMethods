apaTables
================

apaTables 2.0.0

The development version of apaTables R package is hosted here on Github. Current stable version is on the CRAN, see apaTables [here.](https://cran.r-project.org/web/packages/apaTables/index.html)

### Install Stable CRAN Version

``` r
install.packages("apaTables",dep=T)

library(apaTables)
```

### Install Development Version

``` r
install.packages("devtools")

devtools::install_github("dstanley4/apaTables")

library(apaTables)
```

Context
-------

Reproducible research is research for which the numbers reported in the paper can obtained by others using the original data and analysis scripts. (Note that this differs from replicability - the extent to which findings are consistent across samples.) Recent research has revealed a problem with the reproducibility of analyses in many fields. For example, in psychology Nuijten et al. (2015) found that in 50% of articles there was at least once instance of a reported test statistic (e.g., *t*(24)=22.71) being inconsistent with the reported *p*-value. This inconsistency rate suggests there is a major problem with reproducibility in the psychological literature.

My objective in creating the **apaTables** package was to automate the process through which tables are created from analyses when using R. Using **apaTables** ensures that the tables in your manuscript are reproducible.

Although a number of table generation packages exist for R they are typically not useful for psychology researchers because of the need to report results in the style required by the [American Psychological Association](http://www.apa.org); that is, [APA Style](http://www.apastyle.org/products/asc-landing-page.aspx). Consequently, **apaTables** creates [Microsoft Word](https://products.office.com/en-ca/word) documents (.doc files) that contain tables that conform to APA Style.

In many cases it would be necessary to execute additional R commands to obtain all of the statistics needed for an APA Style table. For example, if conducting a regression using the **lm** command the unstandardized regression (i.e., b) weights are reported. Additional commands are needed to obtain standardized (i.e., beta) weights. **apaTables** automatically executes these additional commands to create a table with the required information in Microsoft Word .doc format[1].

Additionally, the [American Statistical Association](http://www.amstat.org) recently released a [position paper](https://www.amstat.org/newsroom/pressreleases/P-ValueStatement.pdf) on the use of *p*-values in research. A component of that statement indicated that "*Scientific conclusions and business or policy decisions should not be based only on whether a p-value passes a specific threshold.*" The Executive Director of the [ASA](http://www.amstat.org) suggested that [confidence intervals should be used to interpret data](http://retractionwatch.com/2016/03/07/were-using-a-common-statistical-test-all-wrong-statisticians-want-to-fix-that/). This statement is consistent with the 1999 [position paper](http://www.apa.org/science/leadership/bsa/statistical/tfsi-followup-report.pdf) from the APA Task Force on Statistical Inference. Consequently, the current version of **apaTables** indicates significance using stars but more importantly reports confidence intervals for the reported effect sizes.

Examples
--------

You can learn how to use apaTables [here](https://dstanley4.github.io/apaTables/articles/apaTables.html).

References
----------

Field, A., Miles, J., Field, Z. *Discovering statistics using R*. Sage: Chicago.

Nuijten, M. B., Hartgerink, C. H. J., van Assen, M. A. L. M., Epskamp, S., & Wicherts, J. M. (2015). The prevalence of statistical reporting errors in psychology (1985-2013). *Behavior Research Methods*. <http://doi.org/10.3758/s13428-015-0664-2>

[1] Technically the tables are in .rtf format. But you should end all files with .doc; this will ensure they are automatically loaded by Microsoft Word
