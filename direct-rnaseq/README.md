---
title: Nanopore direct RNAseq
---
# Evaluation of Nanopore direct RNAseq data in Galaxy

Powered by: <FlatShield label="usegalaxy" message="eu" href="https://usegalaxy.eu"/>

<!--
[Milad Miladi](https://github.com/mmiladi),
[Wolfgang Maier](https://github.com/wm75),
[Florian Heyl](https://github.com/heylf),
[Björn Grüning](https://github.com/bgruening)
-->

<a href="https://www.biorxiv.org/content/10.1101/2020.07.18.204362v1"><img align="right" width="160" src="./img/qrcode.png"></a>

This page serves as a companion to our study describing the transcriptomic and epigenetic analysis of SARS-CoV-2 direct RNA sequencing data using Galaxy:

> [The landscape of SARS-CoV-2 RNA modifications](https://doi.org/10.1101/2020.07.18.204362). Milad Miladi, Jonas Fuchs, Wolfgang Maier, Sebastian Weigang, Nuria Diaz i Pedrosa, Lisa Weiss, Achim Lother, Anton Nekrutenko, Zsolt Ruzsics, Marcus Panning, Georg Kochs, Ralf Gilsbach, Bjoern Gruening. *bioRxiv* 2020.07.18.204362; doi: https://doi.org/10.1101/2020.07.18.204362

Direct RNA sequencing (DRS) using Oxford Nanopore technologies (ONT) enables direct sensing of native RNA molecules.
In the case of SARS-CoV-2 and other coronaviruses this, in turn, enables the quantitative observation of the complex pattern of subgenomic RNA species transcribed *in vivo* from the full viral RNA genome.
At the same time, RNA modifications on the RNA genome and each of the subgenomic RNAs can be detected based on deviations in the electric signal from the expected signal given the reference genome sequence, or from the signal obtained with an *in vitro* transcribed and, thus, unmodified RNA sample.

Up to now, two other studies ([Kim et al.](https://doi.org/10.1016/j.cell.2020.04.011) and [Taiaroa et al.](https://doi.org/10.1101/2020.03.05.976167) ) have explored the scope of SARS-CoV-2 genomic and sub-genomic RNAs using Nanopore DRS.
Our own analysis extends this prior work, by providing data and analyses for three more isolates of SARS-CoV-2 thereby enabling the first comparison of the earlier results obtained for an Asian and an Australian isolate with results for geographically separate European isolates.

In addition, we have developed a set of Galaxy workflows for:

1. [Pre-processing of direct RNAseq data](1-preprocessing),

   which includes

   - the extraction of viral reads from ONT data obtained from cell culture
   - mapping of these reads to the viral genome allowing for spliced alignments in order to be able to detect sgRNA-derived reads

2. [Discovering sgRNA evidence and classifying reads](2-sgrna-detection) as genomic or according to the sgRNA they provide evidence for.

3. Genome/sgRNA-specific [detection of RNA modifications with either Nanocompore or Tombo](3-epigenetics).

With these workflows it becomes possible even for users with very limited background in bioinformatics not only to reanalyze our, but also to analyze their own SARS-CoV-2 direct RNAseq data in a reliable, reproducible and transparent way.


Note: Since submission of the original article we have continued to improve and streamline some of the analysis workflows. For exact reproducibility of the originally reported data we keep [links to the original workflows and analysis histories referred to in version 1 of the manuscript](original-workflows-and-histories.md).

