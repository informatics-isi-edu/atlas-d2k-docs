---
title: Batch Query
permalink: /docs/batch-query/
---

<!-- uncomment when generating PDF in Atom
# Submitting Collections
-->
<!-- comment out when generating PDF in Atom
**[PDF version](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Batch-Query.pdf)**
-->

### Multiple string search
Our search feature supports pattern matching based on PostgresQL regular expression syntax. When you want to search for a disjunction of symbols such as gene names (e.g. `ATP6` or `COX1`), you can use the character `|` to separate between different symbols e.g. `APT6|COX1`. For example, specifying

```
APT6|COX1|Six2
```
in the main search box will returns all the records that have either the sub-string `APT6`, `COX1`, or `Six2` associated with any metadata as the result.

Note:
- There should be no spaces between `|` and individual search strings.
- The search string is not case sensitive.
- Hover over the seach icon (magnifying glass icon next to the search box) to get the tooltip of the search syntax.

### Multiple string search on specific facet
If you want the search to be limited to only a certain property (e.g. NCBI Symbol), you will need to apply the search string to the specific search panel. After the search is specified, select the corresponding checkboxes to be included in the search. Please note that clicking on `Show detail` will open up a window with more choices. You can change the page size. Clicking `All` will select all choices appeared on the page. Clicking `None` will unselect all checkboxes.    

### How to convert a column of gene symbol in a spreadsheet to the search string
Most spreadsheet applications support the concatenation or the text join on a range of cells. For open office and Google Spreadsheet, use the following formula to create the search string.
```
TEXTJOIN(delimiter, ignore_empty, text1, [text2, ...])
Where
  - delimiter: A string, possibly empty, or a reference to a valid string. If empty, text will be simply concatenated.
  - ignore_empty: A boolean; if TRUE, empty cells selected in the text arguments won't be included in the result.
  - text1 - Any text item. This could be a string, or an array of strings in a range.
  - text2, ... [OPTIONAL] - Additional text item(s).

Sample Usage:
  TEXTJOIN(“|“, TRUE, “ATP6”, “COX1”)
  TEXTJOIN(“|”, TRUE, A2:A101)
Where A2:A101 is the cell range containing gene symbols
```
