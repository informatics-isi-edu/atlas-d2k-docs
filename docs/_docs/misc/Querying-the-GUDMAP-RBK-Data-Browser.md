---
title: Querying the GUDMAP RBK Data Browser
permalink: /docs/querying-the-gudmap-rbk-data-browser/
---

This section describes how to use the filtering/faceting sidebar to search GUDMAP/RBK data by gene, anatomy and data attributes. Coming soon, you'll be able to search by function and disease.

# What is a GUDMAP entry?

For ISH and IHC specimen data, entries contain the expression data for a single gene, assayed with a defined probe in a single mouse strain of a single mouse sex at a single stage or time in development. Sex can be unknown (e.g. [RID=N-GNB0](https://www.gudmap.org/chaise/record/#2/Gene_Expression:Specimen/RID=N-GNB0)).

For microarray, entries encompass the expression data for many genes sampled from a single stage or time in development. Sex can be unknown (e.g. [RID=R-ZX6Y](https://www.gudmap.org/chaise/record/#2/Microarray:Series/RID=R-ZX6Y)) or both. Each entry relates to a single sample taken from a single microarray series within the database. So if you search by gene, you'll see all microarray entries that contain that gene on the chip.

# Query by Gene

Enter a gene symbol/name (or synonym) in the search box on the homepage ([https://www.gudmap.org](https://www.gudmap.org)) or by using the menu navigation (_Search > Genes_).

The results include GUDMAP entries that contain information about the expression of the gene or genes of interest. Columns indicate the presence of *Expression Scoring*, *Array Data* or *Imaging* data from specimen (in situ, etc). The *Imaging* column includes representative thumbnails of the imaging data.

In the left sidebar of the results, you may filter results further by these categories:

* NCBI Symbol

* MGI Symbol

* Species

* Synonyms

* Any Data (present, not present)

* Imaging Data (present, not present)

* Array Data (present, not present)

* Scored Expression Data (present, not present)

* Scored Expression Region 

* Assay Type

* Anchor Gene Anatomy

* Marker Gene Anatomy

* Antibody Tests

**Screenshot**

The search automatically assumes a 'wildcard' at the end of the search string; therefore, typing in 'uro' will search for words/symbols beginning with 'uro', e.g. urothelium, urogenital, uroplakin, etc.

## Multiple genes (Batch Query)

To search for multiple genes, use the [Batch Query](Batch-Query) method. Use the search method described above but enter multiple genes separated with a pipe character (|) with _no_ spaces in between. 

This list may contain a mixture of different terms (e.g. MGI accession IDs and MCBI Gene Symbols).

# Query by Anatomy

From the menu navigation, go to *Search* > *Anatomy Terms* and choose either *Anatomy Tree* or *Faceted Search*.

![Navigating to the Anatomy via faceted search](wiki_images/anatomy-faceted.png)

## Anatomy Tree

![Navigating to the anatomy tree](wiki_images/anatomy-tree.png)

This option provides a tree structure view of anatomical terms that conform to the [GUDMAP Ontology](https://www.gudmap.org/resources/ontology/).

Start typing an anatomical region in the search field. In the example below, we're typing "prostate". You may also use the dropdown button to specify a Theiler stage:

![Typing prostate into the search field](wiki_images/querying_2.png)

...and the tree will highlight corresponding term(s). In the following screenshot you'll see part of the tree with all terms related to "prostate".

![image alt text](wiki_images/querying_3.png)

Click a term to go to the corresponding Anatomy records page (we have more details on this page further down the page). 

## Faceted Search

This option takes you directly to the Anatomy section of the Data Browser where you may use the left filter sidebar to choose or search for anatomy regions by *Name* or ontology IDs (ie, `EMAPA:18976`). Click the eye icon of the row you’re interested in to view the corresponding Anatomy record page (see below).

![Screenshot of the Anatomy faceted search](wiki_images/querying_4.png)

## Anatomy record page

Below is an example of an Anatomy record page for the term "cortical renal tubule".

![Example of an anatomy page](wiki_images/querying_5.png)

On the *Contents* sidebar to the right side of the page, you’ll see a list of available data including the following types:

* Specimen Expression Rollup

* Anchor Gene Rollup

* Marker Gene Rollup

* Gene List Rollup

* Mouse Allele Expression

The numbers to the right of the names indicate how many instances of these types of data are available.

### To search for genes annotated with expression *present*, *uncertain* or *not detected* in a given structure(s)

Choose "Specimen Expression Rollup" in the *Contents* list. This table includes GUDMAP/RBK entries that include annotated in situ expression data and microarray data.

* For Specimen (ISH/IHC) 
that contain either a **direct annotation** for the anatomical term specified (whether it is *present*, *uncertain* or *possible*) or an **inferred annotation** for the anatomical term (see below). 

  Each entry includes the relevant symbol for the gene expressed in the queried structure. Symbols are the current standard gene symbols (see NCBI). To better understand the context of your results please see the [tutorial on genitourinary development](https://www.gudmap.org/tutorials/urogenital-dev/).

* For Microarray where the anatomical term specified is the sample material or where sub-components of the anatomical term have been used as sample material. 

  For example, using the term ‘maturing nephron’ for the query will return database entries where the sample was the ‘early proximal tubule’ and entries where the sample was ‘maturing renal corpuscle’. Both these structures are part of the maturing nephron.

## Notes on searching by anatomical terms

Structures are often referred to with a variety of different terms. The predictive text in the anatomy search box on the GUDMAP Gene Expression page will help you enter the correct term.  

However, some structures have common names that begin with different text from the ontology name. For example, "proximal tubule" is represented by the term ‘renal proximal tubule’ in the ontology.  You can easily find the ontology term for a structure by viewing the interactive anatomy ontology tree on the left side of the Boolean Anatomy Search page. This tree is supported by a text string search that will find terms containing a given string. For example, typing ‘proximal’ in the ‘find anatomy component’ box will highlight ‘renal proximal tubule’ in the tree.  If you wish to use a term in the anatomy query on the GUDMAP Gene Expression page, for convenience click on the desired term in the anatomy tree; this will be presented in red on the right; copy the term from here and paste into the anatomy query box on the GUDMAP Gene Expression page. The anatomy query on the GUDMAP Gene Expression page will use this term simply as a text string; this is in contrast to the more advanced Boolean search which distinguishes different items in the tree with the same name as different entities (see help for Boolean Anatomy Search).

Queries can be performed for multiple components by entering terms separated by a pipe (|) character with no space in between (e.g. kidney|ovary). Predictive text is available only for the first term in the list but other valid ontology terms can be added by typing on, using | to separate terms.  Queries with multiple terms are treated as A OR B OR C…

## Inferred annotation

Suppose, for example, the anatomical term 'superficial cellular layer' has been annotated as expression *present* for a particular gene. 

As a consequence, the anatomical term 'urothelium' has 'inferred present' annotation (even though it has not been annotated directly) because 'superficial cellular layer' is a part of the 'urothelium'. Equally, if 'urothelium' was annotated as 'not detected' then its parts, including 'superficial cellular layer' would have 'inferred not detected' annotation.

The original annotations and original expression images are displayed on the page for the corresponding database entry.

# Boolean Anatomy Search

The Boolean Anatomy Search allows complex queries to be constructed to search for **gene expression** based on **selected anatomical structures**. 

The search allows combinations of structures and developmental stages and different combinations of expression found to be *present*, *not detected* and *uncertain*. The search can be applied to a combination of structures or just to one structure. 

For example, to retrieve only genes expressed in a structure, or to compare expression in the same structure at different stages.

For more details, please go to the Boolean Anatomy Search Help Page (LINK).

# Query by Accession ID

Is this still relevant? 

In the **Specimens** search ([https://gudmap.org/chaise/recordset/#2/Gene_Expression:Specimen](https://gudmap.org/chaise/recordset/#2/Gene_Expression:Specimen) or *Search* > *Specimens* in the top menu navigation) you may type in a variety of different accession IDs in the main search bar to view all GUDMAP entries that contain information about the expression relating to that ID. 

![image alt text](wiki_images/querying_6.png)

Accession ID's supported by GUDMAP:

* GUDMAP entry ID's (e.g. GUDMAP:8200, GUDMAP:7720). Worked in Specimens search only

* Ensembl ID (e.g. ENSMUSG00000016458). Worked on Gene search only

* MGI ID (e.g. MGI:98968). Worked on Gene search only

* MA probe ID (e.g. maprobe:4427). Doesn’t seem to be supported anymore

Queries using multiple accession IDs can be performed by separating terms with a pipe character (|) with no spaces (e.g. GUDMAP:7200|MGI:98957). Delete unless we get all access IDs searchable from same recordset

Notes:

* The prefix is not required when using this search. If no prefix is specified then the search will be performed across all accession types.

* When searching using an ID other than GUDMAP ID, only in-situ (ISH & IHC) entries will be returned.

# Query by function (?)

Are we doing this?

The query by function text box on the GUDMAP Gene Expression page can be used to search for genes and probes annotated with a Gene Ontology (GO) Molecular Function,  Biological Process, or Subcellular Location term. This search addresses all in situ expression data in GUDMAP.

The query-string entered into the text box will be used to search the GO ontology for occurrences of this term. For each of the GO terms found a check is done to find all gene products annotated with these terms. A nice explanation of the methods and types of annotation used by GO is the GO Evidence Decision Tree.

The list of gene products gives a list of gene symbols that can then be used to search the GUDMAP database find entries that contain information about the expression of these genes.

NOTE: Searching by function will only return ISH or IHC entries.

# Query by disease (coming soon)

The GUDMAP disease resource is accessible by clicking on Query > Disease or via the Disease menu bar item on the top of the page. This searchable database of associations between genes and diseases of the urogenital system can be queried : 

* by **Disease-gene** associations: Select a disease to find genes associated with this condition or select a gene to search for potential diseases associated with it.

* by **Phenotype-gene** associations: Select a phenotype to find associated genes or select a gene to search for potential phenotypes associated with it.

For detailed examples on finding genes associated with disease and their location and expression in the genitourinary system, please look at the using GUDMAP tutorial and the GUDMAP demos .

Links to GATACA and ToppGene can be found in the left side bar of the GUDMAP disease resource pages.

