# Codes and functions for the  analysis of the *Deinococcus radiodurans* 3C data
This document presents several codes and functions for the processing, visualization and primary analysis of 3C dataset. Lioy et al. released the procedure for analyzing *Escherichia coli* 3C data (https://github.com/koszullab/E_coli_analysis), and we referred to their public code and made some modifications for our research.

There are three main folders, namely data, python_codes and scripts.
## data folder
1. Normalized contact matrix files with three different conditions.
- MAT_scn_wt.txt
- MAT_scn_uv.txt
- MAT_scn_ebfC.txt
2. Genome sequence file and gene annotation file.
- GCF_000008565.1_ASM856v1_genomic.fna
- GCF_000008565.1_ASM856v1_genomic.gff
- new_old_gene_tag.txt
3. Protein-protein interaction pairs file from the STRING database.
- trusted_PPI_pairs.txt
4. Gene differential expression files.
- UV_DEGs_log2_1.csv
- ebfC_DEGs_log2_1.csv
- gene_fpkm.csv
- wt_bin_fpkm.txt
- UV_bin_fpkm.txt
- ebfC_bin_fpkm.txt
5. Constructed genome-scale metabolic model.
- iDR741.xml
5. Folder 'reconstruction_structure_files' containing PDB files for reconstructing chromosome structure.
6. Folder 'result_files' containing CID boundary gene files produced through script 'CID_Boundary_GC_content_and gene.ipynb'.
## python_codes folder
This directory contains several python codes and functions used in the analysis from Lioy et al. (https://github.com/koszullab/E_coli_analysis/tree/master/python_codes). 
## scripts folder
We perform the 3C-seq and flux balance analysis using the following scripts:

- contact_map_and_DI_analyze.ipynb: The contact map were drawn and compared. Identifying CID through directionality index at 100 kb scale.
- CID_Boundary_GC_content_and gene.ipynb: Statistics of GC content of sequences at the boundaries of CIDs and extraction of genes at the boundaries of CIDs.
- wt_scalogram_and_DI.ipynb: This script allows to visualize the dispersion of the contacts signal along the spatial scales for drawing scalogram and calculate the size of CIDs.
- PPI_distance_calculate.ipynb: Calculation of PPI pairs distance.
- correlation_transcription_3C.ipynb: Analysis of correlation between transcription and 3C contacts. 
- exp_level_position.ipynb: Analysis of structural and transcriptional changes at local chromosomal locations.
- Eflux2.ipynb: Metabolic network analysis using E-Flux2 method.
