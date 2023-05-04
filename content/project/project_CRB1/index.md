---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Determining the functional disparty between CRB1 variants causing   LCA and RP"
summary: "Leveraging cutting-edge model systems to further understand CRB1-related eye disease"
authors: [admin]
tags:
  - genomics
  - rare disease
  - genetics
  - bioinformatics
  - CRB1
  - LCA
  - RP
  - retinal organoids
categories: []
share: false
date: 2022-07-05T00:13:01Z
#header:
#  image: "back02.jpg"
#  caption: ""

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: #"Growing CRB1 3D retinal organoids as a disease model"
  focal_point: "Smart"
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
---

*CRB1*-related eye disease is a rare genetic disorder that affects the retina, the light-sensitive layer of tissue at the back of the eye [^1]. The *CRB1* gene provides instructions for making a protein that is essential for the normal development and function of the retina. This protein helps to regulate the number and arrangement of light-sensitive cells in the retina. Variants in  *CRB1* disrupt the normal function of this protein, leading to the death of light-sensitive cells and as a result, people with *CRB1* eye disease experience a progressive loss of vision. There is currently no cure for this disorder [^2].

![*CRB1* genetic variants](crb1-variants2.png "*CRB1* genetic variants *source: gnomAD*")

Leber's congenital atrophy ([LCA](https://eyewiki.org/Leber_Congenital_Amaurosis)) is a form of inherited blindness that is caused by the death of photoreceptor cells in the retina. Retinitis pigmentosa ([RP](https://eyewiki.org/Retinitis_Pigmentosa)) is another inherited blindness that is caused by the degeneration of the retina. Both conditions can result from variants in *CRB1* and may lead to complete blindness. How the distinct phenotypes result from variants in the same gene still remains unclear.

I use model systems to investigate several aspects of *CRB1*-related eye disease:

- Using the zebrafish *crb2a -/-* null model, I am studing how the transcriptome of the retina differences compared to wildtype controls. This has provided us key insights into the molecular changes resulting from loss of *crb2a*, and has identified a novel control mechanism for this disease.


![The zebrafish eye](zebrafish-eye.png "The zebrafish eye")

- Cell lines are often a vital resource for research, especially those generated from tissue kindly provided by patients. We are in the fortunate position of having a patient kindly donate a skin biopsy to allow us to generate induce pluoripotent stem cells (iPSC). We can reprogramme these cells into different cell types and use them for downstream  analysis. Reprogramming into 3D retinal organoids, early eye cups, gives us a fantastic model in which to assess molecular and cellular changes caused by the variants in the *CRB1* gene.

![3D retinal organoid](organoid2.png "3D Retinal Organoid of a *CRB1* line")
![3D retinal organoid](Go-BP.png "Gene Ontology Enrichment Analysis of *crb2a -/-* retina transcrtipomes.")


We hope to assess several *CRB1* patients with different variants to give us an insight into how genetic differences within the same gene could result in the varied phenotype (LCA/RP).

![Wellcome Trust](2000px-Wellcome_Trust_logo.svg_.png "")

[^1]: [What is *CRB1*](https://crb1.org/for-families/faqs/what-is-crb1/)
[^2]: [Clinical trials information](https://www.fightingblindness.org/research/horama-acquires-licensing-rights-to-crb1-gene-therapy-119)

