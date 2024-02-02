# Data Files 

Files for whole genome benchmark sets summary table and figures.
`{REF}_{stvar,smvar}.tsv` and `{REF}_{stvar,smvar}.stats.txt` generated using the `get_bench_metrics.tsv` script. 
Run on workstation in `/defrabb_runs/runs_in_progress/20240109_v0.014_HG002/analysis` directory with the `hlienv` conda environment.

All files compressed using gzip


- `{REF}_{stvar,smvar}.tsv` tables with CHROM, REF, ALT, GT from benchmark vcfs, after filtering variants based size (stvar > 49bp, smvar < 50 bp), and only including variants in benchmark regions.
- `{REF}_{stvar,smvar}.stats.txt` summary stats files generated using `bcftools stats`
- `*.benchmark_bed-summary.tsv` genome coverage calculated using `bedtools summary` generated as part of defrabb run.