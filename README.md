# AGBT 2024 GIAB DeFrABB Poster Presentation

## Title
Genome In A Bottle: New era of assembly-based variant benchmark sets

## Authors

- N.D. Olson
- N. Dwarshuis
- J.M. McDaniel
- J. Wagner
- J.M. Zook


## Abstract
Genome in a Bottle was started over 10 years ago with the goal of developing well-characterized
human genome reference materials for validating genome sequencing and variant calling methods.
GIAB has produced 5 genomic DNA reference materials as well as benchmark sets which are
composed of high confidence variant calls as well as regions confidently identified as homozygous
reference or as high confidence variants. Currently there are 8 whole genome benchmark sets, small
variant benchmarks for 7 individuals including members of an Ashkenazim and Han Chinese trios
along with a structural variant benchmark for one of the individuals. These benchmark sets are
widely used for evaluating variant calling methods as well as training machine learning and deep
learning variant callers. Traditionally these benchmark sets are developed through the integration
of multiple variant calls generated using different sequencing technologies and variant calling algorithms.
However, this process involves mapping reads to a reference, which is limited in its ability to
characterize more complex regions of the genome. With recent advances in sequencing methods
and genome assembly algorithms it is now possible to create high quality diploid de novo genome
assemblies. We have developed a new Snakemake-based pipeline, Defrabb (development environment
for assembly-based benchmarks), that generates high quality whole genome small and structural
variant benchmark sets from assemblies. These assembly-based benchmarks include regions of
the genome that were excluded when using read-mapping-based benchmark generation methods,
such as the highly polymorphic MHC, gene conversions, and more complex SVs. Here we present our
new pipeline along with our first X and Y benchmark set and a draft whole genome SV benchmark
set. The XY benchmark covers 94% of X and 63% of Y, with 87,452 SNP and 24,273 indels. The draft
HG002 SV benchmark for GRCh38 covers ~2,788,000,00 bases with nearly 30,000 variants. These new
assembly-based variant call benchmark sets will allow for the validation of challenging, previously
unbenchmarkable variant calls and can be used to train deep learning models to more accurately
call variants in these challenging regions.


## References


### Publications

- GA4GH small variant benchmarking best practices: Krusche et al. 2019 doi.org/10.1038/s41587-019-0054-x
- GIAB Stratifications: https://doi.org/10.1101/2023.10.27.563846
- XY Benchmark:  https://www.biorxiv.org/content/10.1101/2023.10.31.564997v1.full.pdf
- StratoMod: https://doi.org/10.1101/2023.01.20.524401
- Mosaic Benchmark Poster: https://mdic.org/wp-content/uploads/2018/11/MDIC_AGBT-Poster_FINAL.pdf
- TandemRepeat Benchmark: https://www.biorxiv.org/content/10.1101/2023.10.29.564632v1

### Data

- [GIAB Stratifications v3.3](https://ftp-trace.ncbi.nlm.nih.gov/ReferenceSamples/giab/release/genome-stratifications/v3.3/)
- [HG002 GRCh38 v1.0 XY Benchmark](https://ftp-trace.ncbi.nlm.nih.gov/ReferenceSamples/giab/release/AshkenazimTrio/HG002_NA24385_son/chrXY_v1.0/GRCh38/)
- [GIAB RNAseq](https://ftp-trace.ncbi.nlm.nih.gov/ReferenceSamples/giab/data_RNAseq/)
- [HG002 TandemRepeat Benchmark](https://ftp-trace.ncbi.nlm.nih.gov/ReferenceSamples/giab/release/AshkenazimTrio/HG002_NA24385_son/TandemRepeats_v1.0/GRCh38/)
- [HG002 Draft Whole Genome Small and SV Benchmark](https://ftp-trace.ncbi.nlm.nih.gov/ReferenceSamples/giab/data/AshkenazimTrio/analysis/NIST_HG002_DraftBenchmark_defrabbV0.012-20231107/), this is a work in progress check parent directory for new drafts.

### Tools

- [hap.py](https://github.com/Illumina/hap.py)
- [vcfeval](https://github.com/RealTimeGenomics/rtg-tools)
- [truvari](github.com/spiralgenetics/truvari)
- [hap-eval](https://github.com/Sentieon/hap-eval)
- [vcfdist](https://github.com/TimD1/vcfdist)
- [giab-stratifications](https://github.com/ndwarshuis/giab-stratifications)
- [defrabb](https://github.com/usnistgov/giab-defrabb)
- [adotto](https://github.com/ACEnglish/adotto)
- [laytr](https://github.com/ACEnglish/laytr)
- [StratoMod](https://github.com/ndwarshuis/stratomod)