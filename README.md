# MiRNAbase


This repository contains a dataset for identifying single nucleotide polymorphisms (SNPs) located within genomic regions of human microRNAs (miRNAs).

## Data Sources

The analysis uses publicly available genomic databases:

- **dbSNP (NCBI)** — full human SNP dataset  
- **miRBase** — genomic coordinates of human microRNAs  
- **Human genome reference (GRCh38)**

## Methods

The pipeline performs the following steps:

1. Download the complete SNP dataset from NCBI.
2. Extract SNP genomic coordinates using `bcftools`.
3. Download miRNA coordinates from miRBase.
4. Convert chromosome identifiers to a unified format.
5. Identify overlaps between SNPs and miRNA regions using `bedtools intersect`.
6. Generate a final table of SNPs located within miRNA loci.

## Tools Used

- bcftools
- bedtools
- awk
- wget
- Terminal
