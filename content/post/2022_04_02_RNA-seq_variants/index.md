---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Calling Variants from RNA-seq data"
subtitle: "An updated approach to variant detection in transcriptomes"
summary: "The combination of abundant data resources and cheap sequencing technology has resulted in a vast unexploited resource for single nucleotide polymorphism (SNP) detection."
authors: [admin]
tags: [RNA-seq, Variant, Sequencing, Bioinformatics, Transcriptomics]
categories: []
date: 2022-04-02T16:41:43Z
lastmod: 2022-04-02T16:41:43Z
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: [RNA-seq-bulk, project_GEL]
---
The current gold standard method of choice to study transcriptome expression is RNA-seq. This is commonly used to study gene expression patterns in a number of organisms; including human, animals and plants, in order to further understand genetic mechanisms underlying phenotype determination, diseases and results of environmental changes. Not only can RNA-seq analysis be used for gene expression, transcript modelling including the identification of novel expressed isoforms or alternative exon usage has become more popular. Examination of the long non-coding RNA atlas (lncRNA) and micro RNAs (miRNA) can readily be carried out using specific RNA-seq approaches. Combined with DNA-seq SNPs have been studied with feature expression data to identify expression quantitative trait locus (eQTL) via GWAS mapping or allele-specific expression (ASE) (for example the human GTEx Consortium, 2020). 

With the phenomenon of RNA editing, where a nucleotide change can be observed at the RNA level, post DNA transcription, it is possible that variants can only be observed at the RNA level, absent at DNA level (such as WGS or WES).  Therefore RNA-seq can also detect genomic variants in expressed regions of the genome, in addition to DNA-seq. With the current costs of RNA-seq per sample around £300 for 75M paired end reads (150bp), RNA-seq is an attractive approach for variant discovery.


Although there are clear advantages in using RNA-seq data for coding region SNP detection, it is not commonly carried out. There are a number of hurdles to overcome:
- transcriptome consists of mature/spliced transcripts
- short reads frequently overlap exon-exon junctions
- reads are commonly split using N cigars

There are distinct stages of analysis for variant calling from RNA-seq data. I will try to encompass all of them, so please skip ahead to sections you require.

Assumptions I will make: you have the raw reads processed for base scoring and quality controlled, removed adapters, a reference genome has been downloaded and indexes created for the [STAR](https://github.com/alexdobin/STAR) splice-aware aligner, reads have been aligned using the index with two-pass alignment using STAR. 

Key notes: ensure that ReadGroups have been added to your resulting BAM files - this can either be done within the aligner command with the argument 
```--outSAMattrRGline ID:${sample_id} CN:{SampleCentre} DS:RNAseq LB:{LibraryType} PL:{Platform} SM:${sample_id}```

I am going to skip over the initial steps of quality control (QC) and alignment with STAR, as those are outlined in the RNA-seq workflow I have on github. There are however some key files that should have been generated when processing the reference genome fasta (.fa) and aligner index files. Ensure that the reference .fa is indexed correctly, I recommend [```samtools faidx```](http://www.htslib.org/doc/samtools-faidx.html) and that a dictonary (.dict) file has been created, for example with the [```picard CreateSequenceDictionary```](https://gatk.broadinstitute.org/hc/en-us/articles/4405443616667-CreateSequenceDictionary-Picard-) tool. 

Analysis:
{{< figure src="https://drive.google.com/uc?id=1yLptERtjtDzx36vqAPZCMJgvbhASdsjq" id="wowchemy" >}}

1. QC
2. Alignment
3. Split N Cigar Reads
4. Base quality recalibration
5. Call variants

4. Base Quality Recalibration

-BLURB-

One of the hurdles that you may encounter using the 
```bash

pwd lets go

```
