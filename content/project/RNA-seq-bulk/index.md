---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Transcriptomic analysis of model systems"
summary: "Cross species transcriptome analysis can be a powerful tool for identifying rare disease genes. By looking at the transcriptome of a variety of species, including humans, it is possible to identify genes that are differentially expressed in the diseased state. This can help to identify both disease-causing genes and genes that are involved in the disease process."
authors: [admin]
tags: [RNA-seq, transcriptomics, splicing, RNA, bioinformatics, GEL]
categories: [transcriptomics]
date: 2022-06-01T01:24:50Z
share: false

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""

banner:
  image: "header.png"
  caption: "Image credit: [**Geo**](https://github.com/gcushen/)"

---

Cross species transcriptome analysis can be a powerful tool for identifying rare disease genes. By looking at the transcriptome of a variety of species, including humans, it is possible to identify genes that are differentially expressed in the diseased state. This can help to identify both disease-causing genes and genes that are involved in the underlying processes.

[RNA transcriptomics](https://en.wikipedia.org/wiki/RNA-Seq) is the study of the transcriptome, which is the complete set of RNA molecules, including mRNA, lncRNA, piRNA, and asRNA, that are produced by a cell. Transcriptomics can be used to study the function of genes and to understand how the expression of genes is regulated. RNA-seq data analysis is the process of determining the function and structure of RNA molecules from high-throughput sequencing data, often termed [Next Generation Sequencing (NGS)](https://www.ebi.ac.uk/training/online/courses/functional-genomics-ii-common-technologies-and-data-analysis-methods/next-generation-sequencing/). This data can be used to understand the underlying changes in gene expression, regulation, in relation to disease or treatment states.

Bulk RNA-seq has been the defacto [gold standard](https://www.nature.com/articles/s41598-020-76881-x) used to investigate changes in gene expression, in tissues (including archived samples), cells, and model systems. RNA-seq data analysis involves the identification and characterization of differentially expressed gene or gene sets using a variety of different algorithms.

{{< figure src="go-functional.png" id="go-function" >}}

We use bioinformatics of RNA-seq data to explore the functional relationships between the changes in feature (gene/transcript) expression between conditions. Initially modelling and identifying expression of differentially expressed genes (DEGs) allows us to test numerous hypothesis as to what may be driving these changes. Using enrichment and over-representation analysis allows us to furhter link observed changes between conditions to the underlying molecular defects controlling such changes. 

Using various model systems; including zebrafish mutants, 3D retinal organoid optic cup vesiciles, patient cell lines, iPSC stem cells and standard cell lines, I am interested in how genetic variants in eye disease functionally come about. These diseases include:-
- [CRB1-related Leber Congenital Amaurosis (LCA) and Retinitis Pigmentosa (RP)](https://www.fightforsight.org.uk/get-involved/family-funds-dedicated-groups/teamcrb1/)
- [Ushers Syndrome](https://rarediseases.info.nih.gov/diseases/5440/usher-syndrome-type-2a)
- [MAC (Microphthalmia, Anophthalmia and Coloboma)](https://macs.org.uk/). 
- [RDH12-related retinitis pigmentosa](https://iovs.arvojournals.org/article.aspx?articleid=2711472)
- [Myopia](https://pubmed.ncbi.nlm.nih.gov/34405458/)

{{< figure src="gel-rare-disease.png" id="gel-raredisease" >}}

Using an analagous approach with the [Genomics England 100,000 Genomes rare disease dataset (GEL)](https://www.genomicsengland.co.uk/initiatives/100000-genomes-project/rare-disease), I utilise the RNA-seq data to identify potential novel causative genes from variants of uncertain significance (VUS) in specific patient cohorts.

Bioinformatics is used to term a field of biology that deals with the application of computer techniques to the management and analysis of biological data.
