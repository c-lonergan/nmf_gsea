# nmf_gsea
**Identifying significantly enriched gene sets with NMF-derived metagenes and their difference vectors.**

R markdown demonstrates improved identification of key pathways involved in 3 CNS tumour subtypes: 
 - RNA-seq data is read, annotated, and cleaned.
 - nsNMF algorithm reduces dimensionality into 4 metagenes (incl. normal).
 - Pair-wise difference vectors are calculated, and GSEA results compared with those from each metagene.
 - Difference vectors identify several key pathways that are overlooked by use of metagenes alone. 

To view results, pull repository and extract "...Results.tar.gz" files to load .RData files containing the results of nsNMF decompositions, GSEA results for the decomposed RNA-seq data (Dataset 1), and an additional dataset that has undergone tumour purification (Dataset 2).
Pathway enrichment analysis is summarized in "out/tables" folder, and results are visualised in "out/figures" folder. 
Leading edge genes can also be exported from listed DOSE::gseaResult objects.

The plots below demonstrate that subtracting the normal metagene from the medulloblastoma metagene exposes downregulation of synaptic vesicle cycle pathways in the medulloblastoma samples, where enrichment analysis of the medulloblastoma metagene did not.

Enrichment map plot of metagene M minus metagene N
![Enrichment map plot of metagene M minus metagene N](out/figures/Dataset_1/KEGG/MN_emapplot.png)
Enrichment map plot of metagene M 
![Enrichment map plot of metagene M](out/figures/Dataset_1/KEGG/M_emapplot.png)
Dot plot of metagene M minus metagene N
![Dot plot of metagene M minus metagene N](out/figures/Dataset_1/KEGG/MN_dotplot.png)
Dot plot of metagene M
![Dot plot of metagene M](out/figures/Dataset_1/KEGG/M_dotplot.png)

