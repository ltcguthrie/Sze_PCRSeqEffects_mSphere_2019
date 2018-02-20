## The Influence of High Fidelity DNA Polymerase on 16S rRNA Gene Sequencing

**Background.** Research has identified various methodological steps along the 16S rRNA gene survey pipeline that can change microbial community results. Although cycle number and high fidelity (HiFi) DNA polymerase are studied less often, they are still important sources of bias. Here, we critically examine both cycle number and HiFi DNA polymerase for biases that may influence downstream bacterial community results.  


**Methods.** DNA from fecal samples (n = 4) were extracted using a PowerMag DNA extraction kit with a 10 minute bead beating step and amplified at 15, 20, 25, 30, and 35 cycles using Accuprime, Kappa, Phusion, Platinum, or Q5 HiFi DNA polymerase. Mock communities (technical replicates n = 4) consisting of previously isolated whole genomes of 8 different bacteria were also amplified using the same approach. First, the number of OTUs (Operational Taxonomic Units) were examined for both fecal samples and mock communities. Next, Bray-Curtis index, the error rate, sequence error prevalence, and chimera prevalence were investigated. Finally, the chimera prevalence correlation with number of OTUs was assessed.


**Results.** At 35 cycles there were significant differences between HiFi DNA polymerase for fecal samples (P-value < 0.0001). These HiFi dependent differences in the number of OTUs could be identified as early as 20 cycles in the mock communities (P-value = 0.002). Chimera prevalence varied by HiFi DNA polymerase and these differences were still observed after chimera removal using VSEARCH. Additionally, the chimera prevalence had a strong positive correlation with the number of OTUs and this association was not changed by chimera removal with VSEARCH.


**Conclusions.** Due to HiFi DNA polymerase dependent differences in the number of OTUs and chimera prevalence, common diversity metrics could have values that are not comparable across studies. 



### Overview

	project
	|- README          # the top level description of content (this doc)
	|- CONTRIBUTING    # instructions for how to contribute to your project
	|- LICENSE         # the license for this project
	|
	|- submission/
	| |- study.Rmd    # executable Rmarkdown for this study, if applicable
	| |- study.md     # Markdown (GitHub) version of the *.Rmd file
	| |- study.tex    # TeX version of *.Rmd file
	| |- study.pdf    # PDF version of *.Rmd file
	| |- header.tex   # LaTeX header file to format pdf version of manuscript
	| |- references.bib # BibTeX formatted references
	| |- XXXX.csl     # csl file to format references for journal XXX
	|
	|- data           # raw and primary data, are not changed once created
	| |- references/  # reference files to be used in analysis
	| |- raw/         # raw data, will not be altered
	| |- mothur/      # mothur processed data
	| +- process/     # cleaned data, will not be altered once created;
	|                 # will be committed to repo
	|
	|- code/          # any programmatic code
	|
	|- results        # all output from workflows and analyses
	| |- tables/      # text version of tables to be rendered with kable in R
	| |- figures/     # graphs, likely designated for manuscript figures
	| +- pictures/    # diagrams, images, and other non-graph graphics
	|
	|- exploratory/   # exploratory data analysis for study
	| |- notebook/    # preliminary analyses
	| +- scratch/     # temporary files that can be safely deleted or lost
	|
	+- Makefile       # executable Makefile for this study, if applicable


### How to regenerate this repository

#### Dependencies and locations
* Gnu Make (v3.81) should be located in the user's PATH
* mothur (v1.39.3) should be located in the user's PATH
* sratoolkit (2.8.2-1) should be located in the user's PATH
* R (v.3.4.2) should be located in the user's PATH


#### Running analysis

```
git clone https://github.com/SchlossLab/Sze_PCRSeqEffects_XXXX_2017.git
make write.paper
```
