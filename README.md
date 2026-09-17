
This repository contains the computational pipeline, scripts, and technical resources associated with the manuscript:

> ** AI-Powered Discovery of Novel RNA Viruses from the Permafrost of a 14,300-Year-Old Pleistocene Wolf**  
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

Pipeline Overview
The pipeline includes the following major steps:

Quality filtering — fastp v0.23.4

Host removal — Bowtie2 against host reference genomes

De novo assembly — MEGAHIT v1.2.9

Viral screening

Diamond BLASTx against viral RefSeq

HMMER v3.3 with Pfam, vFam, PalmScan, pVOG profiles

Lucaprot deep-learning screening for divergent sequences

Phylogenetic analysis — MAFFT, trimAl, IQ-TREE2

Structural validation — AlphaFold2 / ColabFold, PyMOL TM-align

Authentication

RNA degradation profiling

Logan planetary-scale SRA database screening

Requirements
Software
Tool	Version	Purpose
fastp	0.23.4	Quality filtering
Bowtie2	2.5.0+	Host removal
MEGAHIT	1.2.9	De novo assembly
Diamond	2.1.0+	BLASTx screening
HMMER	3.3	Profile HMM searches
Prodigal	2.6.3	ORF prediction
MAFFT	7.475	Sequence alignment
trimAl	1.4	Alignment trimming
IQ-TREE2	2.0+	Phylogenetics
CAP3	10.2015	Contig reassembly
CD-HIT	4.8.1	vOTU clustering
PyMOL	2.5+	Structural alignment
Python Packages
text
biopython>=1.79
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.5.0
scikit-learn>=1.0.0
AlphaFold2
Structural predictions were generated using ColabFold or AlphaFold2. Please install according to the official documentation.

Installation
bash
git clone https://github.com/Syed-Zaheer-ud-Din/Noval-RNA-Viruses-Extinct-species-.git
cd Noval-RNA-Viruses-Extinct-species-

# Recommended: create a conda environment
conda env create -f environment.yml
conda activate paleovirology
