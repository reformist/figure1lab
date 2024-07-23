# figure1lab
## Week 1: Key Scientific Question
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
The KSQ is essentially asking if we can repurpose two existing drugs to treat other cancers through evaluating similarities in single cell expression.

## Resources:
[Definition of Cancer Cellines](https://www.cancer.gov/publications/dictionaries/cancer-terms/def/cancer-cell-line)
[Dr. Aviv Regev Talk
](https://www.youtube.com/watch?v=Wk5QHySlMXU)https://www.news-medical.net/life-sciences/What-is-VEGF.aspx
https://www.cancer.org/cancer/types/breast-cancer/understanding-a-breast-cancer-diagnosis/breast-cancer-her2-status.html

