---
title: Querying by Gene
permalink: /docs/query-by-gene/
---

One of the most common ways users want to search is by gene or genes of interest.

**On this page:**
- [Searching by gene name or symbol](#searching-by-gene-name-or-symbol)
  - [Batch querying](#batch-querying)
- [Available filters for genes](#available-filters-for-genes)

## Searching by gene name or symbol

Enter a gene symbol/name (or synonym) in either of the following ways:

- Use the search box on the homepage ([https://www.atlas-d2k.org](https://www.atlas-d2k.org)) (See Figure 1)
- Use the menu navigation (_BROWSE DATA > Gene Search_) to go to the [Gene page](https://www.atlas-d2k.org/chaise/recordset/#2/Common:Gene?pcid=page) and either use the _Gene_ facet in the left sidebar or type in the gene name in the field above the search results

![Screenshot of using the search field on the home page with sox10]({{ "/assets/img/search-gene-home.png" | relative_url }})
_Figure 1: Using the search field on home page with "sox10"_

The results include GUDMAP records that contain information about the expression of the gene or genes of interest and any available related data in our repository.

The *Available Expression Data* and *Representative Images* columns indicate the kinds of data available for that gene.

![Screenshot of the results page]({{ "/assets/img/sox10-results-zoom.png" | relative_url }})
_Figure 2: Zoomed in view of the results page after doing a gene search for "sox10"_


### Batch querying

You can also search for multiple genes at the same time. See [Batch Querying](../batch-query/) for more information.

## Available filters for genes

The [filtering sidebar](../filtering-sidebar/) allows you to narrow you search by the following filtering categories:

| Filter category                                        | Use this filter to search by...                                                                                 |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Gene Symbol                                       | NCBI Symbol                                                                                                    |
| Species                                           | Model organism                                                                                                 |
| Any Expression Data (Available, Not available)    | Available records that include any expression data.                     |
| Imaging Data (Available, Not available)           | Available records that include any imaging data.                        |
| Scored Expression Data (Available, Not available) | Available records that include any scored expression data.              |
| Array Data (Available, Not available)             | Available records that include any microarray data.                     |
| scRNASeq Visualization Data                       | Available records that include any single cell RNA-Seq visualizations.. |
| Synonyms                                          | Known synonyms for genes proteins.                                                                   |
| MGI Symbol                                        | Gene symbols used by the Mouse Genome Informatics Database (MGI).                                |
| Scored Anatomical Region                          | Available anatomical regions with scored expression data.                                    |
| Specimen Assay Type                               | Assay types for specimen data such as in-situ hybridization and immunohistochemistry.                |
| Antibody Tests                                    | Available test results for antibodies.                                             |
{: .table.compact }
