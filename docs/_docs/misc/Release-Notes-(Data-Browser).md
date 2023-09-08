---
title: Release Notes (Data Browser)
permalink: /docs/release-notes-data-browser/
---


This page chronicles the updates made to the Data Browser for gudmap.org and rebuildingakidney.org - starting with 9/25/2018.

# Release 2019-03-26

* Unified data model for all types of imaging data. Now you can see all images under "Specimen" page. 

* Deployed Treeview visualization to visually display the scored expression annotation associated with a mouse specimen. For example: [Specimen N-GHTR](www.atlas-d2k.org/id/N-GHTR). 

* Boolean Anatomy Search ([https://www.atlas-d2k.org/](https://staging.rebuildingakidney.org/deriva-webapps/boolean-search/)[deriva-webapps/boolean-search/](https://staging.rebuildingakidney.org/deriva-webapps/boolean-search/)) is now available on the navigation bar. Click Search, then Boolean Anatomy Search to get to the app. Click an "eye" icon on the page for more information. 

* Sequencing Data 

    * Extend the model to support visualization images and applications. Check out [the studies with visualization images](https://www.atlas-d2k.org/chaise/recordset/#2/RNASeq:Study/*::facets::N4IghgdgJiBcDaoDOB7ArgJwMYFM6JAEsIAjdafEAJQDkBBAZRwEcQAaEANUKTTABtCALzAAXQiggB9BqLRQAnlIBmAaxwKQAXQC+bUOlFk0FBNXpNWHbrwHCxE6Tb6CR4yVLoAHL4KwOPNQ1tPWoASQARbQ4IFFEpCDR+fjhRDDQcHV0gA@sort(RMT::desc::,RID)).

    * Unified data model for scRNA-Seq and bulk RNA-Seq. All sequencing experiments now require Replicates which capture the information about the bio-specimen. Single_Cell_Metrics will only contain statistic information and will be linked to a specific Replicate.  

    * Extend the model to take dbGaP_Accession_ID for human-protected sequencing files. 

* Enabled the repository to accept Antibodies and Protocol data from KPMP

* UX improvements

    * Added a link from the Array heatmap page to the raw array data, so users can download data if needed.

    * Addressed broken URLs. 

    * Changed menu bar navigation from hovering to clicking in order to expand sub menus which will enable touch-screen access. 

    * Automatically scroll to the top after creating/updating records. 

    * Fixed bugs related to Table of Content on the record detail page. 

    * New and expanded Help section.

# Release 2018-12-03
* Anatomy improvements

    * Reverted to GUDMAP (EMAPA) vocabulary (Uberon was not as robust as we’d hoped, so now we are reverting to our own vocabulary and _*we*_ are updating Uberon)

    * Improved linkage by converting expression data to use the same terms as appear elsewhere in the database (previously, they used EMAPS terms)

    * "Rolled up" expression data (so a search for expression in the bladder, for example, will match expression data in any part of the bladder)

    * Simpler interface for adding terms (for data submitters)

    * Normalized species and developmental stage terms

    * Linked anatomical terms to developmental stages ("starts-at" and “ends-at” relationships)

* Improved Anatomical Terms Treeview display of mouse anatomical terms, now based on different stages ([https://www.atlas-d2k.org/deriva-webapps/treeview/](https://www.atlas-d2k.org/deriva-webapps/treeview/))

* Gene UX improvement

    * Searching by Gene now returns records with data by default.

    * You can filter genes based on different types of GUDMAP expression data (e.g. Expression Scored, Array Data, Imaging Data) using the left sidebar. Gene search results include columns that indicate presence of Expression Scored and Array Data as well as Imaging data.

    * Improved performance on the Gene detail page.

    * Heatmap x-labels are displayed vertically instead of slanted at 45-degrees.  

* UI improvements

    * Make the "loading…" indicator more visible so that users can be quickly informed whether the detail page has finished loading

    * Added more tool-tips

* Record edit tool improvement (for data submitters):

    * Batch copy: allow users to easily set a value of a field associated with a selected set of records at once (for example, setting the Curation Status to "Release" on all replicates associated with an RNASeq study)

# Release 2018-09-25
Updates to the user interface:

- When you use the Gene search form on the homepage, it now searches only on the NCBI Symbol and its synonyms. This will reduce false positives in the search results.

- When you click Search by Gene link, the results will by default only display genes with ATLAS-D2K gene expression data. We have also added a few more facets on this page in the left sidebar. 

- Searching by Anatomical Terms will by default only display terms with gene expression data. We have also added a few more facets on this page in the left sidebar.

- Data quality improvements: We have worked with lab members to clean existing data, and added the Record Status Detail field to the Specimen page to provide hints when data are missing (note this is only visible if you are logged in - see below).

- Anonymous users can no longer see the Record Status, Curation Status, or Record Status Detail columns.

Bug fixes:

- Heatmap: Fixed the label truncation issue; we also now provide a link to view the heatmap in Full Screen mode.

- File Upload: Addressed upload failures that were due to long delays of the wide area network (e.g. from Australia to US).
