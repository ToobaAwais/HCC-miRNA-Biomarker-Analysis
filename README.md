# HCC-miRNA-Biomarker-Analysis

Integrative bioinformatics analysis of tissue and serum microRNAs (miRNAs) as biomarkers for hepatocellular carcinoma (HCC) progression and survival, using public data from TCGA and GEO.

## Publication
Jabri A, Mhannayeh A, Alsharif M, Taftafa B, **Mujtaba T**, Akbar A, Abu-zaid A, Mir TA, Khan MI, Ahmed F, Arora I, Yaqinuddin A.
**Integrative analysis of tissue and circulating miRNAs as biomarkers for progression and survival in hepatocellular carcinoma.**
*Non-coding RNA Research*, 16, 167–177 (2026). [doi:10.1016/j.ncrna.2025.11.002](https://doi.org/10.1016/j.ncrna.2025.11.002)

```bibtex
@article{jabri2026hcc,
  title   = {Integrative analysis of tissue and circulating miRNAs as biomarkers for progression and survival in hepatocellular carcinoma},
  author  = {Jabri, Abdullah and Mhannayeh, Abdulaziz and Alsharif, Mohamed and Taftafa, Bader and Mujtaba, Tooba and Akbar, Arshiya and Abu-zaid, Ahmed and Mir, Tanveer Ahmad and Khan, Mohammad Imran and Ahmed, Firoz and Arora, Itika and Yaqinuddin, Ahmed},
  journal = {Non-coding RNA Research},
  volume  = {16},
  pages   = {167--177},
  year    = {2026},
  doi     = {10.1016/j.ncrna.2025.11.002}
}
```

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

## Data availability
All data are public: TCGA-LIHC via the [GDC Data Portal](https://portal.gdc.cancer.gov/) and serum miRNA data from [GEO GSE113740](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE113740). No patient-identifiable data are used.
