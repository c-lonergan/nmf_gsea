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

The plots below demonstrate that subtracting the normal metagene from the medulloblastoma metagene exposes downregulation of the synaptic vesicle cycle pathway hsa04721 in the medulloblastoma samples, where enrichment analysis of the medulloblastoma metagene did not.

emapplots: MN vs M

<img src="https://user-images.githubusercontent.com/72213939/129490964-f7a16c5c-ee8b-4b55-97bd-67d615c99ab5.png" width="45%"></img> <img src="https://user-images.githubusercontent.com/72213939/129490966-7194596a-e4fb-4dd1-b07b-821c2e0291f6.png" width="45%"></img> 

dotplots: MN vs M

<img src="https://user-images.githubusercontent.com/72213939/129491345-52f2e3f5-2ba0-490e-8a30-146e8cde2c5e.png" width="45%"></img> <img src="https://user-images.githubusercontent.com/72213939/129491351-0ccbc0ad-2f8b-4700-8174-32f8cad861a8.png" width="45%"></img> 

cnetplots: MN vs M

<img src="https://user-images.githubusercontent.com/72213939/129491425-216bb022-d961-4c85-a0a0-655135c98420.png" width="45%"></img> <img src="https://user-images.githubusercontent.com/72213939/129491427-42f0bbbb-f3af-4ab7-99b5-925ef7de2d2c.png" width="45%"></img> 

