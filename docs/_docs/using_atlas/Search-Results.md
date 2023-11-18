---
layout: page
title: Using the Search Results page
---

**On this page:**
- [Anatomy of a search page](#anatomy-of-a-search-page)
- [Using the filtering sidebar](#using-the-filtering-sidebar)
  - [Selecting filters](#selecting-filters)
  - [Searching attributes within the sidebar](#searching-attributes-within-the-sidebar)
  - [Expanding/collapsing filters](#expandingcollapsing-filters)
  - [Clearing filters](#clearing-filters)
- [Main search results](#main-search-results)
  - [Searching across columns](#searching-across-columns)
  - [Sorting columns](#sorting-columns)
- [How search works when typing free text](#how-search-works-when-typing-free-text)



## Anatomy of a search page

![screenshot of the landing page](search-page-example.png){:.screenshot}

Above is a typical search results page. Common elements are:

1. Filtering sidebar
2. Filters (which display attributes chosen through the filtering sidebar)
3. Search bar above the results for free text search.
4. Search results based on filters.


## Using the filtering sidebar

The filtering sidebar allows you to narrow your search results by various data attributes and metadata - such as *Species* (mus musculus) and *Assay Type* (ISH) in the example above.

Selecting and de-selecting attributes in any of the facets will filter the results to show only data with those attributes.

![Zoomed in view of sidebar](facet-panel-search.png){:.screenshot.screenshot-sm}

*Zoomed in view of sidebar*


### Searching attributes within the sidebar

A filter displays up to 10 attributes. When there's more than 10, there are a couple of options for finding the one you're looking for.

#### **Search in the filter**

Use the small search box within the filter to search across those attributes only.

The following example shows a user looking through Specimen records who wants to find `proximal tubule` within the regions listed in the "Anatomy" filter.

Note how suggested matches are displayed as the user types.

![animation of searching within Anatomy filter](proximal-tubule-filter-search.gif){:.screenshot}

#### **Use the "Show more" window**

Click the "Show More" link to pull up a modal window where you can browse through all attributes and their descriptions.

In the following example, the user searches just the term `tubercle` to see what's available.

After reading the descriptions, they select both `genital tubercle of male` and `genital tubercle of female` and click *Submit* to see available specimen data for both.

![animation of using the Show More window](tubercle-showmore-search.gif){:.screenshot}

Tips:
- Selecting `All on page` will select all checkboxes that appear in the window.
- Clicking `None on page` will de-select all checkboxes in the window.
- You may also use the search field to narrow down your choices by typing in free text.

### Expanding/collapsing filters

If the filtering sidebar is long, you can manage which filters are shown by clicking the down and up arrow, as shown below, to expand and collapse the filters:

![animation of expanding and collapsing filters](expand-collapse-filters.gif){:.screenshot}

### Clearing filters

If you want to clear a filter, click the `X` icon next to the filter's name.

You can also click "Clear all filters" to remove them all.

![animation of clearing filters](clear-filters.gif){:.screenshot}
