# ChIP-Sequencing
This project presents a complete ChIP-seq analysis pipeline for identifying and functionally annotating histone H3K27ac enrichment sites in human K562 leukemia cells. H3K27ac is a histone modification associated with active enhancers and promoters, making it a key marker for gene regulation and transcriptional activation.
**Objective:**
To analyze ChIP-seq data for H3K27ac in K562 cells, annotate enriched peaks, extract high-confidence target genes, perform functional enrichment, and visualize regulatory regions associated with important leukemia-related genes such as MYC, GATA1, and TP53.

**Tools & Technologies**
HOMER – Peak annotation and gene mapping
BEDTools / samtools – File manipulation (BED, BAM)
g:Profiler – Gene Ontology (GO), Reactome, KEGG enrichment
IGV (Integrative Genomics Viewer) – Genomic visualization
awk / bash / pandas – Filtering, scoring, and data extraction

**Data Source**
ChIP-seq datasets were obtained from the ENCODE project:
https://www.encodeproject.org/experiments/ENCSR000AKP/
H3K27ac ChIP BAM--ENCFF867JTP--Aligned reads (K562)
Input control BAM--ENCFF600THN--Control input reads
narrowPeak file--ENCFF153YGA--High-confidence peaks

**Analysis Steps**
Environment Setup: HOMER, samtools, bedtools installed on Ubuntu
Data Download: BAM and BED files from ENCODE
Peak Annotation: Using annotatePeaks.pl with HOMER (hg38 genome)
Filtering: Peaks with score ≥ 1000; unique gene extraction
Gene List: Top 1000 high-confidence genes selected
Functional Enrichment: g:Profiler used to identify enriched pathways
Visualization: IGV used to explore H3K27ac signal near key genes (e.g., MYC, GATA1)

Results Summary
Total Peaks Identified: 43,034
Annotated Genes: ~22,000
High-score Genes (score = 1000): 5,603
Top Genes Used in Enrichment: 1,000
Enriched Functions: Transcription regulation, chromatin organization, cell cycle

**Key Genes Identified**
MYC – Master regulator of cell proliferation and metabolism
GATA1 – Essential for erythroid differentiation
These genes showed strong H3K27ac signal, indicating transcriptional activity in K562 leukemia cells.
