---
title: Querying the ATLAS-D2K Data Browser
permalink: /docs/querying-the-atlas-d2k-data-browser/
---

This section describes many ways to search ATLAS-D2K data:

## Table of Contents

- [What is a data record in ATLAS-D2K?](#what-is-a-data-record-in-atlas-d2k)
- [Query by Gene](#query-by-gene)
  - [Multiple genes (Batch Query)](#multiple-genes-batch-query)
- [Query by Anatomy](#query-by-anatomy)
  - [Searching by Anatomy Tree (for mouse anatomy)](#searching-by-anatomy-tree-for-mouse-anatomy)
  - [Anatomy: Faceted Search](#anatomy-faceted-search)
  - [Anatomy record page](#anatomy-record-page)
    - [To search for genes annotated with expression *present*, *uncertain* or *not detected* in a given structure(s)](#to-search-for-genes-annotated-with-expression-present-uncertain-or-not-detected-in-a-given-structures)
  - [Notes on searching by anatomical terms](#notes-on-searching-by-anatomical-terms)
  - [Inferred annotation](#inferred-annotation)
- [Boolean Anatomy Search](#boolean-anatomy-search)

## What is a data record in ATLAS-D2K?

For [ISH](https://www.atlas-d2k.org/chaise/recordset/#2/Gene_Expression:Specimen/*::facets::N4IghgdgJiBcDaoDOB7ArgJwMYFM6JHQBcAjdafEAcRwhwH0BRADwAcMckkBLFCEADQgAyqxxZuAW1r0AglzABPegBVFY+gDMA1jkUgAugF8hAJQCSAEUNCsACxTdcSSgEYAbAFoATJYBipoZGxkA?pcid=navbar/record&ppid=1z9l2sm51epk28x71ulk1nx1) and [IHC](https://www.atlas-d2k.org/chaise/recordset/#2/Gene_Expression:Specimen/*::facets::N4IghgdgJiBcDaoDOB7ArgJwMYFM6JHQBcAjdafEAcRwhwH0BRADwAcMckkBLFCEADQgAyqxxZuAW1r0AglzABPegBVFY+gDMA1jkUgAugF8hAOTDTDQrAAsU3XEkoBJABIBhQ0eNA?pcid=navbar/record&ppid=1z9l2sm51epk28x71ulk1nx1) specimen data, a data record contains the expression data for a single gene, assayed with a defined probe in a single mouse strain of a single mouse sex at a single stage or time in development. Sex can be unknown (e.g. [RID=N-GNB0](https://www.atlas-d2k.org/id/N-GNB0)).

For microarray, a data record encompasses the expression data for many genes sampled from a single stage or time in development. Sex can be unknown (e.g. [RID=R-ZX6Y](https://www.atlas-d2k.org/id/R-ZX6Y)) or both. Each record relates to a single sample taken from a single microarray series within the database. So if you search by gene, you'll see all microarray entries that contain that gene on the chip.

## Query by Gene

Enter a gene symbol/name (or synonym) in the search box on the homepage ([https://www.atlas-d2k.org](https://www.atlas-d2k.org)) or by using the top-level menu navigation (_Data > Gene_).

The results include records that contain information about the expression of the gene or genes of interest. The column "Available Expression Data" indicates the presence of *Expression Scoring*, *Array Data* or *Imaging* data from specimen (in situ, etc). The *Imaging* column includes representative thumbnails of the imaging data.

In the left sidebar of the results, you may filter results further by these categories:

* Gene Symbol

* Species

* Synonyms

* Any Expression Data (yes, no)

* Imaging Data (yes, no)

* Scored Expression Data (yes, no)

* Array Data (yes, no)

* scRNA-Seq Visualization (yes, no)

* mRNA-Seq Visualization (yes, no)

* Synonyms

* MGI Symbol

* Scored Anatomical Region

* Specimen Assay Type

* Antibody Tests

The search automatically assumes a 'wildcard' at the end of the search string; therefore, typing in 'uro' will search for words/symbols beginning with 'uro', e.g. urothelium, urogenital, uroplakin, etc.

### Multiple genes (Batch Query)

To search for multiple genes, use the [Batch Query](../batch-query) method. Use the search method described above but enter multiple genes separated with a pipe character ( &#124; ) with _no_ spaces in between. For example:

> APT6&#124;COX1&#124;Six2

This list may contain a mixture of different terms (e.g. MGI accession IDs and MCBI Gene Symbols).

## Query by Anatomy

From the menu navigation, go to _Data > Anatomy_ and choose either *Anatomy: Facet Search* or *Anatomy: Tree View*.

### Searching by Anatomy Tree (for mouse anatomy)

Go to the [Anatomy Tree view](https://www.atlas-d2k.org/deriva-webapps/treeview/).

![Navigating to the anatomy tree]({{ "/assets/wiki_images/anatomy-tree.png" | relative_url }})

This option provides a tree structure view of anatomical terms that conform to the GUDMAP Ontology.

Start typing an anatomical region in the search field. In the example below, we're typing "prostate". You may also use the dropdown button to specify a Theiler stage:

![Typing prostate into the search field]({{ "/assets/wiki_images/querying_2.png" | relative_url }})

...and the tree will highlight corresponding term(s). In the following screenshot you'll see part of the tree with all terms related to "prostate".

![image alt text]({{ "/assets/wiki_images/querying_3.png" | relative_url }})

Click a term to go to the corresponding Anatomy records page (we have more details on this page further down the page).

### Anatomy: Faceted Search

You can reach the [Anatomy faceted search page here](https://www.atlas-d2k.org/chaise/recordset/#2/Vocabulary:Anatomy@sort(RID)).

This is the Anatomy section of the Data Browser where you may use the left filter sidebar to choose or search for anatomy regions by *Name* or ontology IDs (ie, `EMAPA:18976`). Click the View icon of the row you’re interested in to view the corresponding Anatomy record page (see below).

![Screenshot of the Anatomy faceted search]({{ "/assets/wiki_images/querying_4.png" | relative_url }})

### Anatomy record page

Below is an example of an Anatomy record page for the term "cortical renal tubule".

![Example of an anatomy page]({{ "/assets/wiki_images/querying_5.png" | relative_url }})

On the *Sections* sidebar to the right side of the page, you’ll see a list of available data including the following types:

* Specimen Expression Rollup

* Anchor Gene Rollup

* Marker Gene Rollup

* Gene List Rollup

* Mouse Allele Expression

The numbers to the right of the names indicate how many instances of these types of data are available.

#### To search for genes annotated with expression *present*, *uncertain* or *not detected* in a given structure(s)

Choose "Specimen Expression Rollup" in the *Sections* list. This table includes ATLAS-D2K entries that include annotated in situ expression data and microarray data.

* For **Specimen (ISH/IHC)** that contain either a **direct annotation** for the anatomical term specified (whether it is *present*, *uncertain* or *possible*) or an **inferred annotation** for the anatomical term (see below).

  Each entry includes the relevant symbol for the gene expressed in the queried structure. Symbols are the current standard gene symbols (see NCBI). To better understand the context of your results please see the [tutorial on genitourinary development](https://www.atlas-d2k.org/tutorials/urogenital-dev/).

* For **Microarray** where the anatomical term specified is the sample material or where sub-components of the anatomical term have been used as sample material.

  For example, using the term ‘maturing nephron’ for the query will return database entries where the sample was the ‘early proximal tubule’ and entries where the sample was ‘maturing renal corpuscle’. Both these structures are part of the maturing nephron.

### Notes on searching by anatomical terms

Structures are often referred to with a variety of different terms. The predictive text in the "Tissue (Anatomical Source)" filter on the [Specimen search page](https://www.atlas-d2k.org/chaise/recordset/#2/Gene_Expression:Specimen) will help you enter the correct term.

However, some structures have common names that begin with different text from the ontology name. For example, **proximal tubule** is represented by the term **renal proximal tubule** in the ontology.  You can easily find the ontology term for a structure by viewing the interactive anatomy ontology tree on the left side of the [Boolean Anatomy Search page](../boolean-anatomy-search/). This tree is supported by a text string search that will find terms containing a given string. For example, typing **proximal** in the "find anatomy component" box will highlight **renal proximal tubule** in the tree.  

Queries can be performed for multiple components by entering terms separated by a pipe (|) character with no space in between (e.g. **kidney|ovary**). Predictive text is available only for the first term in the list but other valid ontology terms can be added by typing on, using the pipe character to separate terms.  Queries with multiple terms are treated as **A OR B OR C**.

### Inferred annotation

Suppose, for example, the anatomical term "superficial cellular layer" has been annotated as expression *present* for a particular gene.

As a consequence, the anatomical term "urothelium" has the *inferred present* annotation (even though it has not been annotated directly) because "superficial cellular layer" is a part of the urothelium. Equally, if urothelium was annotated as *not detected* then its parts, including superficial cellular layer would have the *inferred not detected* annotation.

The original annotations and original expression images are displayed on the page for the corresponding database entry.

## Boolean Anatomy Search

The Boolean Anatomy Search allows complex queries to be constructed to search for **gene expression** based on **selected anatomical structures**.

The search allows combinations of structures and developmental stages and different combinations of expression found to be *present*, *not detected* and *uncertain*. The search can be applied to a combination of structures or just to one structure.

For example, to retrieve only genes expressed in a structure, or to compare expression in the same structure at different stages.

For more details, please go to the [Boolean Anatomy Search page](../boolean-anatomy-search/).
