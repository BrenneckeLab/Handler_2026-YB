# A Naïve RNA Sampling Core Enables Adaptive piRNA Specificity Against Transposable Elements

**Handler_2026-YB**

This repository provides figure-generation code, rendered analysis reports, plasmid maps, and links to additional computational resources associated with the study:

> **A Naïve RNA Sampling Core Enables Adaptive piRNA Specificity Against Transposable Elements**

## Overview

Genome defense systems must target selfish genetic elements while avoiding host-gene silencing. The piRNA pathway does so in part by preferentially producing piRNAs from transposon-rich cluster transcripts, yet the basis of this selectivity remains incompletely understood.

Comparing somatic and germline piRNA pathways in *Drosophila*, we identify a basal piRNA-processing system with low intrinsic selectivity that distinct mechanisms refine into transposon specificity. In somatic cells, Yb channels uridine-rich RNAs into piRNA biogenesis. Because LTR retrotransposon genomes are strongly adenosine-biased, their antisense transcripts are correspondingly uridine-rich, providing a molecular basis for high piRNA output from antisense retrotransposon-rich clusters such as *flamenco*.

In the germline, broad transcriptome sampling generates initial piRNAs, but only piRNAs encountering complementary transcripts seed ping-pong amplification. Host mRNAs generally lack cytoplasmic antisense partners, whereas transposon mobility can generate complementary transcripts through new insertions, resulting in the preferential amplification of transposon piRNAs.

We propose that piRNA clusters are specialized antisense transposon RNA sources, while nucleotide-biased precursor selection and complementarity-dependent amplification confer specificity and adaptability to emerging transposon threats.

## Repository contents

```text
Handler_2026-YB/
├── Fig1.Rmd
├── Fig1.html
├── Fig2.Rmd
├── Fig2.html
├── Fig3.Rmd
├── Fig3.html
├── Fig4.Rmd
├── Fig4.html
├── Fig5.Rmd
├── Fig5.html
├── Fig5_ping-pong.Rmd
├── Fig5_ping-pong.html
├── Plasmid Maps/
├── LICENSE
└── README.md
```

The `.Rmd` files contain the R code used to generate figure panels. The corresponding `.html` files are rendered reports containing the code, output, and embedded plots.

## Figure-generation code

| Figure | R Markdown source | Rendered report |
|---|---|---|
| Figure 1 | [Fig1.Rmd](Fig1.Rmd) | [Fig1.html](Fig1.html) |
| Figure 2 | [Fig2.Rmd](Fig2.Rmd) | [Fig2.html](Fig2.html) |
| Figure 3 | [Fig3.Rmd](Fig3.Rmd) | [Fig3.html](Fig3.html) |
| Figure 4 | [Fig4.Rmd](Fig4.Rmd) | [Fig4.html](Fig4.html) |
| Figure 5 | [Fig5.Rmd](Fig5.Rmd) | [Fig5.html](Fig5.html) |
| Figure 5 ping-pong analysis | [Fig5_ping-pong.Rmd](Fig5_ping-pong.Rmd) | [Fig5_ping-pong.html](Fig5_ping-pong.html) |

The rendered reports, including their embedded graphs, can also be viewed or downloaded from:

[Figure reports and raw analysis output](https://brenneckelab.imba.oeaw.ac.at/Publication_Data/2026_Handler_YB/Figures_raw-data/)

Because the HTML reports are rendered documents, they can be inspected without installing R or the required R packages.

## OSC genome resources

This study used the genome assembly of ovarian somatic cells (OSCs).

- [OSC genome data](https://brenneckelab.imba.oeaw.ac.at/Publication_Data/2025_Handler_OSC-genome/)
- [UCSC Genome Browser session](https://genome-euro.ucsc.edu/s/Brennecke%2DLab/OSC_r1.01_Handler_et.al._2025)

The genome-data directory contains the OSC genome archive, UCSC Genome Browser hub files, and associated Apptainer resources.

## Plasmid maps

Plasmid maps and sequences related to the manuscript are available in the [`Plasmid Maps`](Plasmid%20Maps) directory.

For each construct, files are generally provided in the following formats:

- `.dna` — SnapGene plasmid-map format
- `.gb` — GenBank annotated sequence format
- `.fa` — FASTA sequence format

The directory includes constructs associated with:

- U-ramp sensor variants
- Variable U-content sensors
- Neutral-UTR sensors
- Translation sensors
- *traffic jam* UTR constructs
- Selection cassettes

## Associated analysis repositories

### piRNA-biogenesis sensor analysis

[Handler_2026-YB_sensorAnalysis](https://github.com/BrenneckeLab/Handler_2026-YB_sensorAnalysis)

Scripts for processing and quantifying piRNA-biogenesis sensor libraries, including sense and antisense read assignment and generation of summary tables.

### Transposable-element nucleotide composition

[Yb_2026](https://github.com/RippeiHayashi/Yb_2026)

Scripts and associated sequence resources used to analyze nucleotide and codon composition in *Drosophila* protein-coding genes and Gypsy-family LTR retrotransposons. The repository also contains scripts and output for phylogenetic analysis of Gypsy POL reverse-transcriptase domains.

### Sequencing-data processing and annotation

[AnnotationPipeline](https://github.com/BrenneckeLab/AnnotationPipeline)

Pipeline used for the primary analysis of Illumina sequencing data, including small-RNA annotation, genome mapping, transposon quantification, browser-track generation, ping-pong analysis, and differential gene-expression analysis.

## Reuse of the analysis code

The R Markdown files document the code used for figure generation. They reference analysis tables generated during upstream processing. Therefore, cloning this repository alone may not provide every intermediate input required to rerun all notebooks from beginning to end.

For inspection of the complete rendered analyses and plots, use the supplied HTML reports or the externally hosted reports linked above.

To clone the repository:

```bash
git clone https://github.com/BrenneckeLab/Handler_2026-YB.git
cd Handler_2026-YB
```

To render an individual notebook when its required input files and R packages are available:

```r
rmarkdown::render("Fig1.Rmd")
```

## Citation

If you use code, plasmid sequences, genome resources, or processed data from this repository, please cite the associated manuscript:

> Handler et al. *A Naïve RNA Sampling Core Enables Adaptive piRNA Specificity Against Transposable Elements.*

Publication details and a persistent identifier should be added here when available.

When reusing code from one of the associated repositories, please also cite or reference that repository as appropriate.

## Contact

For questions or additional information, please contact:

[dominik.handler@imba.oeaw.ac.at](mailto:dominik.handler@imba.oeaw.ac.at)

## License

This repository is distributed under the [MIT License](LICENSE).
