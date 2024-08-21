# figure1lab
## Week 1: Key Scientific Question
Reference Research Paper: https://www.nature.com/articles/s41588-020-00726-6
In biotech, the goal is to lengthen patients’ lifespan and/or increase their quality of life.
The idea and data: 
Using available scRNA-seq data from cancer cell lines, how would I explore the use of the following FDA-approved antibody therapies in additional cancers?
Trastuzumab: Targets HER2 and is used in the treatment of HER2 positive breast and gastric cancers
Bevacizumab: Targets VEGF and is used for a variety of cancers, including colorectal, lung, glioblastoma, breast, living, and kidney cancer.

# Questions I have:
If both of these therapies are monoclonal antibodies, do they target the same or similar antigen(s)?
# What is HER2 and VEGF?
HER2 is a protein that’s related to breast cancer cells growing quickly. They grow faster than breast cancer cells who are HER2 negative. HER2 is related to triple negative breast cancer, which is cancer that is HER2-, ER- and PR negative which means that hormone therapy and drugs that target HER2 aren’t as effective.
VEGF (vascular endothelial growth factor) is a protein that promotes new blood vessel growth. Cancer can increase production of VEGF which can result in more nutrients being directed to the tumor, allowing it to grow quicker and remain alive, and ultimately metastasizing without intervention.
How can I use scRNA-seq to elucidate insights from these therapies?
By finding scRNA-seq data from these cell lines that are affected with a drug, perhaps it’ll be possible to see which responds better against HER2 and VEGF.
Why do we need to use scRNA-seq instead of bulk-RNA-seq?
scRNA-seq is useful here because we can investigate specific cell types and cell state transitions versus a tissue level analysis. This means that we can look at possible differences between early stage cancer cell lines and late stage cancer cell lines.
# Questions Dean prompted:
## What are cancer cell lines and why do we use them?
Cancer cell lines are cells that continuously multiply if given the proper resources. This implies they don’t have the same cell cycle checkpoints as normal cells. We use them to study cancer because it’s more ethical than treating humans directly and still provide an accurate understanding of drug efficacy and cancer targets
## What is scRNA-seq, and why is it useful for cancer drug development?
scRNA-seq provides information about cells at a granularity never before seen. Since DNA is largely the same cell to cell, and protein capture per cell is a rigorous challenge, RNA is used to interpret cell health and for cellular understanding. Prior to scRNA-seq, bulk-RNA-seq would collect pools of cells and burst them to get an overall sense of the RNA content in tissue. At this resolution level, however, it’s easier to identify heterogeneous cell populations in a cancer and different cell states, providing a deeper understanding of cancer and as a result, a better way to develop drugs for it.
	
## Restating the KSQ:
The KSQ is essentially asking how it would be possible to use the dataset to perform drug repurposing.

## Resources:
[Definition of Cancer Cellines](https://www.cancer.gov/publications/dictionaries/cancer-terms/def/cancer-cell-line)
[Dr. Aviv Regev Talk
](https://www.youtube.com/watch?v=Wk5QHySlMXU)https://www.news-medical.net/life-sciences/What-is-VEGF.aspx
https://www.cancer.org/cancer/types/breast-cancer/understanding-a-breast-cancer-diagnosis/breast-cancer-her2-status.html

-----------------------------------------------------------------------------
## Week 2: Reading the Paper
# How did the authors handle the potential caveat of co-culturing cell lines before profiling by scRNA-seq? Why do you think that caveat was or was not adequately addressed?
Co-culturing means growing the cells in in the same petri dish, which means they may have interacted with each other in the CCLE (Cancer Cell Line Encyclopedia) pool but not HNSCC (Head and Neck Squamous Cell Carcinoma) pool. The authors mention that this is acceptable because the patterns of heterogeneity were as similar between cell lines from the same pool as they were between cell lines from different pools. In the supplementary information, they mention running a one-way ANOVA test, which is used to analyze variance and that there was minimal effects.
By looking at the supplementary figures, 1b makes it seem that the non-negative matrix factorization scores (still trying to understand what that means–is this good for identifying features?) are similar for co-cultured vs not co-cultured, which support the authors’ points. I assume 1e displays a hierarchical cluster showing the individually clustered cell line with a co-cultured cell line for most connections, so I think that fits the narrative. Not sure how 1c and 1d fit the narrative because it only shows heterogeneity for the single cell lines but not the co-cultured cell lines. While the data looks reasonable, I still wonder if certain cancer lines might interfere with each other more than others and this isn’t answered fully.
# The authors identified discrete subpopulations of cells within a subset of individual cell lines (Fig. 2A-B). What might be the reason why some cell lines have these discrete subpopulations while others do not?
The reason why they’re in different clusters is because there are groups of cells with significantly different RNA expression (I know there are settings to perform tSNE that result in more separation of clusters (perplexity) but I assume the authors didn’t overuse it). To have different RNA expression within the same cell line implies that there were some genetic mutations in some of the cells that didn’t occur in the other. Perhaps certain cell lines mutate more than others. Further, since they were co-cultured, there’s a chance that certain cells closer to the other culture were influenced by their environment differently than the ones that were further away.
# What are Recurrent Heterogeneous Programs (RHPs) and how were they defined?
In the paper, they’re defined as “comparison of the NMF programs, based on their shared genes, emphasized clusters of similar programs, allowing us to define the consensus of each cluster, which we termed RHPS of gene expression, as they were heterogeneous across cell lines”
To my understanding, NMF identifies patterns/programs within the gene expression of a cell line, and these programs are clustered together. A consensus of these cluster captures the tendencies of all the programs/patterns within the cluster. The fact that they were recurrent means that the programs/patterns are seen across multiple cell lines (thus why cell cycle related RHPs were identified as cell cycle is crucial for cell division and these cancer cell lines are replicating frequently), and heterogeneous means that all the programs consisted of the same genes, their expression patterns were different.
# How do the identified RHPs relate to in vivo programs of heterogeneity in tumors, and what evidence supports this relationship?
The authors state that each RHP was detected across at least 8 different cell lines and from at least 4 different pools, implying that these RHPs were ingrained in tumors and not just in a specific cell line. Authors also had in vitro RHPs and in vivo RHPs. The authors mention that seven of the ten cell line RHPs (in vitro) were similar to the in-vivo RHPs, as seen with the overlap of significant genes and high correlation of cell scores. Specifically, the authors show that in vitro RHPs can replicate in vivo RHPs, at least in epithelial-mesenchymal transitions.
# Where can you download the scRNA-seq data as shown in Figure 1B?
The data can be found on the Broad Institute’s single cell  website:
https://singlecell.broadinstitute.org/single_cell/study/SCP542/pan-cancer-cell-line-heterogeneity
# Further questions
# Why is it such a large deal that in vitro cell lines mirror in vivo ones--I thought this was the hope in using cell lines in the first place? 
Further, just because in-vitro cell lines have similar genetic patterns doesn't necessarily imply that treatments that work on cell lines would work on in-vivo cell lines due to the complexities of drug delivery and other body environmental factors.
# Why did the authors use tSNE instead of UMAP?

# Additional Notes
It makes sense that the authors matched the scRNA-seq cells with the most similar bulk RNA-seq cell line because it's a sanity check that the cells are the expected types.





