# ReadFastQC
Catch useful informations (e.g. the "Name", the "Date", the "Total Sequences", the "Sequences flagged as poor quality",  the "Sequence length", the "%GC" and the adapters content) into FastQC html files created by the FastQC tool.

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

Run this to catch the information for one FastQC file :

``` r
FastQCresults("HI.4112.002.D710---D501.X18_R2_fastqc.html") # for old FastQC version <2019
New_FastQCresults("HI.4112.002.D710---D501.X18_R2_fastqc.html") # for new FastQC version > 2019
```

Run this to catch all information for all FastQC files and print it in a file ("**FastQCanalysis.csv**") :
``` r
FastQCresultsForAll() # for old FastQC version <2019
New_FastQCresultsForAll() # for new FastQC version > 2019
```
Run this to obtain all adapters content of all FastQC in one pdf file ("**Adapters content.pdf**"), but before you will need to unzip all files :

``` r
adapter()
```

Run this to obtain all the per base quality of all FastQC in one pdf file ("**Per base quality.pdf**"), but before you will need to unzip all files  :

``` r
bquality()
```

And that's it ! ;)

# Update 2020/03/17

For new version of FastQC, lunch:

``` r
New_FastQCresults("HI.4112.002.D710---D501.X18_R2_fastqc.html")
New_FastQCresultsForAll()
```
