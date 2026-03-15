# MiRNAbase


This repository contains a dataset for identifying single nucleotide polymorphisms (SNPs) located within genomic regions of human microRNAs (miRNAs).

The project was developed as part of a student research project for the **"Young Biologist" conference** and demonstrates how large genomic datasets can be analyzed using bioinformatics tools.

## Project Goal

The goal of this project is to build a curated dataset of SNPs that overlap with human microRNA regions. Such variants may influence miRNA structure or function and therefore could potentially affect gene regulation and predisposition to socially significant diseases.

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
- Unix shell

## Output Dataset

The final dataset:
