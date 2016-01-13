# RFS-DNAseq
workflow for analysis of ref4-3 suppressor whole-genome sequencing 

(steps 1 and 2 were performed by the Purdue sequencing center, presumably could use same code as for SNP detection from Wide-seq data) 
1. Bowtie2 alignment of reads 
  FASTQ -> BAM
2. Samtools detection of SNPS 
  BAM -> SAM -> VCF
3. candidate genes were viewed using the Integrated Genome Viewer (IGV)

Mutants with no SNPs in candidate genes (i.e. rfs2-1) were then processed using 
4. SNPSift to filter for homozygous, EMS SNPs
5. SNPEff to annotate SNP effects (gene, nucleotide/AA substitution, Low/High/Moderate effect, etc.) 
6. SNP effects were then parsed into an Excel readable formate using C script from Charles Addo Quaye (Dilkes Lab)
