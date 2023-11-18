---
title: Querying by Anatomy (Tree View and Facet View)
permalink: /docs/query-by-anatomy/
---

**On this page:**
- [Finding anatomy search options](#finding-anatomy-search-options)
- [Using the Anatomy Tree](#using-the-anatomy-tree)
- [Searching anatomical terms with Faceted Search](#searching-anatomical-terms-with-faceted-search)
- [Elements of the Anatomy record page](#elements-of-the-anatomy-record-page)

## Finding anatomy search options

From the menu navigation, go to *BROWSE DATA* > *Anatomy Terms Search* and choose either *Anatomy Facet Search* or *Anatomy Tree View*.

![Navigating to the Anatomy searches via the menu]({{ "/assets/img/anatomy-menu.png" | relative_url }})

## Using the Anatomy Tree

This option provides a tree structure view of anatomical terms that conforms to the [GUDMAP Ontology](https://www.atlas-d2k.org/resources/ontology/). You can use this visualization to understand the hierarchy of anatomical regions and see any data in GUDMAP related to that region.

Start by typing an anatomical region in the search field. You may also use the dropdown button to specify a [Theiler stage](https://www.atlas-d2k.org/resources/theiler-stages/) to indicate the age.

As a result, the tree will highlight corresponding term(s).

In the example below, we're typing "proximal tubule" and using Theiler stage TS23 (15dpc):

![Animation of typing prostate into the search field and seeing results]({{ "/assets/img/anatomy-tree-view-animation.gif" | relative_url }})

Click a term to go to its [Anatomy record page](#elements-of-the-anatomy-record-page).

In the following screenshot, we are seeing the resulting record for "[early proximal tubule EMAPA:28003](https://www.atlas-d2k.org/chaise/record/#2/Vocabulary:Anatomy/RID=14-4YS0)" (the ID corresponds to the [GUDMAP Ontology identifier](https://www.atlas-d2k.org/resources/ontology/).)

![Navigating to the Anatomy searches via the menu]({{ "/assets/img/anatomy-record.png" | relative_url }})

## Searching anatomical terms with Faceted Search

Choosing *Anatomy Terms Search* takes you directly to the [_Anatomy_ section](https://www.atlas-d2k.org/chaise/recordset/#2/Vocabulary:Anatomy) of the Data Browser.

From here you can use use the [filtering sidebar](../filtering-sidebar/) or the free text search to find anatomy records by *Name* or [ontology IDs](https://www.atlas-d2k.org/resources/ontology/) (ie, `EMAPA:18976`).

Click the "View" icon of the row you’re interested in to view the corresponding Anatomy record page (see below).

![Screenshot of the Anatomy faceted search]({{ "/assets/img/anatomy-faceted-search.png" | relative_url }})

## Elements of the Anatomy record page

Let's search for "cortical renal tubule" from the anatomy faceted search:

![Example of searching for cortical renal tubule]({{ "/assets/img/cortical-renal-tubule-search-animation.gif" | relative_url }})

Here is the resulting Anatomy record page:

![Screenshot of the Anatomy faceted search]({{ "/assets/img/cortical-renal-tubule-search.png" | relative_url }})

On the *Sections* sidebar to the left side of the page, you’ll see a list of available data including:

| Section                    | Description                                             |
|----------------------------|---------------------------------------------------------|
| Part of                    | Indicates "parent" regions to this anatomical region. For example, pelvic urethra is part of urethra.  |
| Includes                   | Indicates "children" regions to this anatomical region. For example, pelvic urethra includes epithelium of pelvic urethra. |
| Specimen Expression Rollup | TODO                                                    |
| Anchor Gene Rollup         | TODO                                                    |
| Marker Gene Rollup         | TODO                                                    |
| Gene List Rollup           | TODO                                                    |
| Mouse Allele Expression    | TODO                                                    |
{: .table.compact }
