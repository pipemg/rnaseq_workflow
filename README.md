## RNASeq workflow

This repository will eventually contain the standardized analysis protocol used in the [Resendis lab](http://resendislab.inmegen.gob.mx). At the moment this is still in planning and benchmarking phase.

## Steps and tool candidates

### Visualization and QC

- IGV -> https://www.broadinstitute.org/igv/
- FastQC -> www.bioinformatics.babraham.ac.uk/projects/fastqc/

### Read mapping/alignment

- STAR -> https://github.com/alexdobin/STAR
- kallisto -> https://pachterlab.github.io/kallisto/
- TopHat -> https://ccb.jhu.edu/software/tophat/index.shtml
- salmon -> http://combine-lab.github.io/salmon/
- HTSeq -> http://www-huber.embl.de/HTSeq/
- RSubread -> https://bioconductor.org/packages/release/bioc/html/Rsubread.html
- StringTie -> http://www.nature.com/nbt/journal/v33/n3/full/nbt.3122.html
- RSEM -> https://github.com/deweylab/RSEM/ (used by TCGA)

### Normalization and Differential Expression

- DeSeq2 -> https://bioconductor.org/packages/release/bioc/html/DESeq2.html
- edgeR -> https://www.bioconductor.org/packages/3.3/bioc/html/edgeR.html
- sleuth (for kallisto and salmon) -> https://pachterlab.github.io/sleuth
- limma + voom -> https://www.bioconductor.org/packages/release/bioc/html/limma.html

### Benchmarks

- DE gene calling -> http://www.genomebiology.com/2013/14/9/R95
  limma voom wins, edgeR and DeSeq also good, cuffdiff very high FPR
- DE Gene calling (high replicates) -> http://arxiv.org/pdf/1505.02017v2.pdf
  edgeR, DeSeq and limma the best but very conservative
- Counting -> http://arxiv.org/pdf/1505.02710.pdf (kallisto paper)
  kallisto best, RSEM 2nd, Tophat + Cufflinks worst
- Isoform quantification -> http://mikelove.github.io/eurobioc2015
  In accuracy alpine (not readu yet) best, kallisto and RSEM 2nd, cufflinks the worst

### Workflow options

- Bowtie2 + Tophat2 + Cufflinks
- STAR + RSEM
- STAR/Tophat2 + HTSeq
- Kallisto
- Salmon

