---
title: Which genes are expressed in multiple regions?
permalink: /docs/gene-expression-multiple-regions/
---

Using the [Boolean Anatomy Search](../boolean-anatomy-search/), you can choose multiple anatomical regions and then query for expression of one or more genes. In this example, we'll be using the Boolean Anatomy Search to answer the question:

> **Which genes are expressed in the renal medullary interstitium, outer medullary interstitium and inner medullary interstitium?**

**On this page:**
- [Step 1: Go to the Boolean Anatomy Search app](#step-1-go-to-the-boolean-anatomy-search-app)
- [Step 2: Set up a Boolean query](#step-2-set-up-a-boolean-query)
- [Step 3: Search Specimen records](#step-3-search-specimen-records)
- [Video demonstration](#video-demonstration)

## Step 1: Go to the Boolean Anatomy Search app

In the top-level menu choose _BROWSE DATA_ > _Anatomy_ > _Boolean Anatomy Search_.

Which opens the Boolean Anatomy Search app:

[![screenshot of the Boolean Anatomy Search app](boolean-search-app.png){:.screenshot}](boolean-search-app.png)

## Step 2: Set up a Boolean query

You can find the [full documentation page here](../../boolean-anatomy-search/), but on this page we'll be demonstrating a particular query.

We will set up three different conditions - each for one of the anatomical regions where we want to know if expression strength is present: the renal medullary interstitium, outer medullary interstitium and inner medullary interstitium.

* In the left hand section, in the search field above the tree, type `renal medullary interstitium`. When you see the term appear in the tree, click the term to populate the condition box on the right side.

  Make sure the "Strength" field is set to “present”

* Click the plus (+) sign to add another condition.

* Repeat this step with the terms `outer medullary interstitium` and `inner medullary interstitium`. You should now have three condition on the right side of the screen:

**Note:** If you see no results for an anatomical region, make sure you are using the appropriate developmental stage in the dropdown box at the top of the anatomy tree.

[![screenshot of the boolean conditions](boolean-conditions.png){:.screenshot}](boolean-conditions.png)


## Step 3: Search Specimen records

Now click the "Search Specimen" button to search all gene records that show expression present in those regions.

[![screenshot of the specimen search results from the query](boolean-search-specimen-results.png){:.screenshot}](boolean-search-specimen-results.png)

In the search results, you’ll see in the _Genes_ facet in the left sidebar the following genes, which indicate we have data that shows the expression of these genes in all three regions: _Crym, Wnt4, Ptch1_.

## Video demonstration

Here is a video demonstrating the above steps:

<iframe width="560" height="315" src="https://www.youtube.com/embed/FCYddOXGhGk" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
