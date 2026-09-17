### AI-Powered Discovery of Novel RNA Viruses from the Permafrost of a 14,300-Year-Old Pleistocene Wolf

# Computational Pipeline for Paleotranscriptomic Mining of Ancient RNA-seq Data

This repository contains the computational pipeline, scripts, and technical resources associated with the manuscript:

> **Paleotranscriptomic mining of extinct species reveals novel RNA viruses from a 14,300-year-old Pleistocene canid**  
> Syed Zaheer ud Din, Q. Wu  
> *bioRxiv* (2026). DOI: [TO BE ADDED]

**For scientific background, results, and discussion, please read the preprint on bioRxiv:**  
**[https://www.biorxiv.org/](https://www.biorxiv.org/)** *(link/DOI to be updated)*

This README is intended to provide technical documentation only: installation, dependencies, usage, and data access. It does not summarize or discuss the scientific findings.

---

## Repository Contents

```text
.
├── README.md
├── LICENSE
├── environment.yml
├── data/
│   ├── supplementary_table1_sra_libraries.tsv
│   ├── contig1_duamitovirus_tumati.fasta
│   ├── contig2_orthocuvulavirus_tumati.fasta
│   └── phiX174_control.fasta
├── scripts/
│   ├── 01_quality_filtering.sh
│   ├── 02_host_removal.sh
│   ├── 03_de_novo_assembly.sh
│   ├── 04_viral_screening_diamond.sh
│   ├── 05_hmm_profiles.sh
│   ├── 06_lucaprot_screening.py
│   ├── 07_phylogenetic_analysis.sh
│   ├── 08_alphafold2_validation.py
│   ├── 09_degradation_profiling.py
│   └── 10_logan_screening.sh
├── results/
│   ├── phylogenetic_trees/
│   ├── alphafold_models/
│   ├── degradation_plots/
│   └── logan_analysis/
└── figures/
    ├── figure1_pipeline_overview.png
    ├── figure2_sra_distribution.png
    ├── figure3_tumat_location.png
    ├── figure4_contig1_phylogeny.png
    ├── figure5_contig2_phylogeny.png
    ├── figure6_structural_analysis.png
    ├── figure7_phix174_control.png
    ├── figure8_degradation_profiles.png
    └── figure9_logan_screening.png
