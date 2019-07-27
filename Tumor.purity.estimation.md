Tumor purity estimation

A loss of heterozygosity (LOH) score was calculated as the absolute difference between the allele fraction in tumor and germline sample for heterozygous germline SNVs. For example, an SNV from a region with a clonal single copy number loss and 100% tumor purity would have an LOH score of 0.5. We used LOH scores from SNVs within tumor copy-neutral LOH or heterozygous copy number loss regions (CNV value of between 0 and −1) to estimate tumor purity for all whole genome sequencing (WGS) samples. We assumed that the real genomic copy number of a single copy loss in x% of tumor cells could be estimated as −x/100 with an LOH value of x/(400−2x). Assuming the remaining LOH signal came from CN-LOH (CN-LOH in x% tumor cell resulted in a LOH value of x/(100 × (2-CNA))), the tumor content in a region could be estimated as the sum of the fraction with copy number loss and fraction with CN-LOH by: 2 × ai + (CNA)/2 × (1–2 × ai).

Using tumor content estimates from various regions within the genome, we performed an unsupervised clustering analysis using the mclust package (version 3.4.8; https://cran.r-project.org/web/packages/mclust/index.html) in R (version 2.11.1; https://www.r-project.org/). The CNV/LOH based tumor purity of the sample was defined as the highest cluster center value among all clusters. We further ran the mclust algorithm on mutant allele fractions for somatic SNVs in diploid regions without LOH. The MAF based tumor purity of the sample was defined as the highest cluster center value among all clusters. The final tumor purity is defined as the larger of the CNV/LOH based estimate and the MAF-based estimate (X Chen et al. in preparation; code available upon request).