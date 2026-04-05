# 16S rRNA Microbiome Analysis with Mothur

This repository contains a reproducible workflow for the analysis of Illumina paired-end 16S rRNA sequencing data using **Mothur**.

The pipeline was developed during my MSc thesis and demonstrates a complete microbiome preprocessing workflow from raw FASTQ files to OTU distance matrix generation.

---

## Pipeline Overview

This workflow performs:

- Paired-end read assembly
- Quality filtering
- Dereplication
- Alignment to SILVA reference database
- Chimera detection and removal
- Pre-clustering to reduce sequencing noise
- Abundance filtering
- Distance matrix generation for downstream analysis

---

## Repository Structure

```text
Microbiome-16S-mothur-pipeline
│
├── workflow/
│ └── mothur_workflow.md
│
├── scripts/
│ └── script-16S-microbiome-analysis.txt
│
├── example_logs/
│ └── mothur_log_snippet.txt
│
└── README.md

```

## Requirements

- Linux environment
- Mothur (v1.44+)
- SILVA reference database

---

## How to Run

Launch mothur and execute the commands from:

scripts/script-16S-microbiome-analysis.txt


---

## Output

The workflow produces:

- Cleaned and filtered 16S sequences
- Chimera-free dataset
- OTU distance matrix (0.03 cutoff)

These outputs was used for:
- Alpha diversity
- Taxonomy assignment
- Functional annotation

---

## Note

Raw sequencing data are not included due to size and privacy constraints.  
This repository focuses on workflow reproducibility and documentation.

---

## Author

Eleni Terpsidou  
MSc Bioinformatics & Computational Biology
