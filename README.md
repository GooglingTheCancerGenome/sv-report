# sv-report
Evaluation of multiple SV callers

Our aim is to assess the performance of the structural variants (SV) callers that are part of the [sv-callers](https://github.com/GooglingTheCancerGenome/sv-callers) workflow:
* [DELLY](https://github.com/dellytools/delly)
* [LUMPY](https://github.com/arq5x/lumpy-sv)
* [Manta](https://github.com/Illumina/manta)
* [GRIDSS](https://github.com/PapenfussLab/gridss)

To quantify the ability of each caller to detect SVs, we use multiple ground truth datasets. These are collections of SVs that have been validated with multiple sequencing technologies and through comparison with indipendent datasets. Here is a tentative list:
1. The pilot genome NA12878 from [Genome in a Bottle (GiaB) Consortium](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4896128/)
   - 30x downsampled paired end BAM file [RMNISTHS_30xdownsample.bam](http://bit.ly/2DCuMYt)
   - Deletion and insertion sets from the analysis with [svclassify](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-016-2366-2), source: svclassify [Supplemental Data](http://bit.ly/2E9uNUL):
     - Deletions: 'Personalis_1000_Genomes_deduplicated_deletions.bed'
     - Insertions: 'Spiral_Genetics_insertions.bed'
2. The COLO829 dataset of the Hartwig Medical Foundation
   - samples from [Craig et al., 2016](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4837349/)
