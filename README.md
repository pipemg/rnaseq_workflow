## RNASeq workflow

This repository will eventually contain the standardized analysis protocol used in the [Resendis lab](http://resendislab.inmegen.gob.mx). At the moment this is still in planning phase and benchmarking phase.

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

### Normalization and Differential Expression

- DeSeq2 -> https://bioconductor.org/packages/release/bioc/html/DESeq2.html
- edgeR -> https://www.bioconductor.org/packages/3.3/bioc/html/edgeR.html
- sleuth (for kallisto and salmon) -> https://pachterlab.github.io/sleuth

