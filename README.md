# HCC-miRNA-Biomarker-Analysis

Integrative bioinformatics analysis of tissue and serum microRNAs (miRNAs) as biomarkers for hepatocellular carcinoma (HCC) progression and survival, using public data from TCGA and GEO.

## Why this matters
HCC is a leading cause of cancer death, and it's usually caught late because there aren't good non-invasive biomarkers for early detection. This project looks for miRNA signatures — in both tumor tissue and blood serum — that could flag disease progression earlier and more reliably than current markers.

## Data
- **TCGA-LIHC**: tumor and matched normal liver tissue miRNA expression (~425 samples)
- **GEO (GSE113740)**: serum miRNA expression across normal, chronic hepatitis, cirrhosis, and HCC patients

## Methods
- Differential expression analysis (limma-trend)
- Survival analysis (Kaplan-Meier + Cox regression)
- Functional enrichment (GO / KEGG pathway analysis)
- miRNA–gene target network construction
- Clinical subgroup analysis (tumor stage, metastasis status)
- Correlation of serum miRNAs with AFP levels and disease stage

## Key findings
- Identified a focused set of significantly dysregulated miRNAs in HCC tumor tissue vs. normal liver
- Several miRNAs showed independent prognostic value in survival analysis, including some associated with poor outcomes and one with a protective effect
- Serum miRNAs correlated with tumor stage and AFP levels, suggesting potential as non-invasive biomarkers for monitoring disease progression
- Enrichment analysis pointed to cancer-relevant pathways (PI3K-Akt, MAPK signaling) as likely mechanisms

## Tools used
R, Python, limma, survival/lifelines, clusterProfiler, DAVID, networkx

## Repo contents
- `/code` — analysis scripts
- `/plots` — key visualizations (volcano plots, heatmaps, survival curves)
- `/results` — output tables

---
*This project uses only publicly available, de-identified data (TCGA, GEO). Built as an independent bioinformatics project to demonstrate end-to-end NGS/omics data analysis.*
