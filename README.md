# ReadFastQC
Catch useful informations (e.g. the "Name", the "Date", the "Total Sequences", the "Sequences flagged as poor quality",  the "Sequence length", the "%GC" and the adapters content) into FastQC html files created by Galaxy.

Installation from GitHub and loading
------------------------------------

``` r
# may be useful : install.packages("devtools")
library(devtools)
install_github("PLStenger/ReadFastQC")
library("ReadFastQC")
```

Quick Start
-----------

Galaxy give you many FastQC files in zip.
Unzip it in a folder.

Got to **R**, don't forget to "**Get your working directory**" into this previous folder.

Run this to catch the information for one FastQC file generated by Galaxy:

``` r
FastQCresults("HI.4112.002.D710---D501.X18_R2_fastqc.html")
```

Run this to catch all information for all FastQC files generated by Galaxy and print it in a file ("**FastQCanalysis.csv**"):
``` r
FastQCresultsForAll()
```
Run this to obtain all adapters content of all FastQC create by Galaxy in one pdf file ("**Adapters content.pdf**"):

``` r
adapter()
```

And that's it ! ;)
