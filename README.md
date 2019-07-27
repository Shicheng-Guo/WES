### WES: Whole-exome sequencing to identify novel drive mutation for human cancers

#### Update
* 07/27/2019, [MutationalPatterns](https://bioconductor.org/packages/release/bioc/html/MutationalPatterns.html) enter into the pipeline in BIRC10-LC and CHG1
* 07/26/2019, [sequenza](https://cran.r-project.org/web/packages/sequenza/index.html) enter into the pipeline in BIRC10-LC and CHG1
* 01/12/2019, [maftools](https://bioconductor.org/packages/release/bioc/html/maftools.html) enter into the pipeline in BIRC10-LC and CHG1



#### To-Do-List
* [MixClone](https://github.com/uci-cbcl/MixClone): A mixture model for inferring tumor subclonal populations




#### Method
We detected somatic SVs from WGS using [CREST](https://www.ncbi.nlm.nih.gov/pubmed/21666668), and performed integrative SV/CNA detection using [CONSERTING](https://www.nature.com/articles/nmeth.3394) to identify subclonal or complex SVs linked to CNAs. For comparison purposes, we also performed CNA analysis on WES using the [Sequenza algorithm](https://www.ncbi.nlm.nih.gov/pubmed/25319062)


