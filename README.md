# Preprocessing of 72 MeRIP-seq Samples for Unified Methylation Region Construction

This repository documents the full data-processing and quality-control pipeline used to process 72 MeRIP-seq samples and retain 29 high-quality samples for downstream analyses.  
The scripts and configuration files here reproduce the computational workflow from raw public SRA accessions to final, QC-passed methylation peak calls.

> **Note:** Raw sequencing data are **not stored in this repository** because of their size.  
> All source data are publicly available through the NCBI SRA and can be re-downloaded using the scripts provided.

---

## 📘 Overview

Each biological sample includes a pair of sequencing runs:
- Input sample (background control)  
- IP sample (immunoprecipitated m⁶A-enriched fraction)

The processing pipeline performs:
1. Download of raw `.sra` files  
2. Conversion to FASTQ format  
3. Alignment to the GRCh38 reference transcriptome  
4. Conversion to sorted and indexed BAM files  
5. Annotation database construction
6. Peak calling using TRESS 
7. Quality control using GC-bias assessment and DRACH motif enrichment, resulting in 29 retained samples.

---

## 🧭 Directory Structure
