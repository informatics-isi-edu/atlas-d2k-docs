---
title: Submitting Data Collections
permalink: /docs/data-collections/
---

<!-- uncomment when generating PDF in Atom
# Submitting Collections
-->
<!-- comment out when generating PDF in Atom
**[PDF version](/docs/data-collections.pdf)**
-->

This page provides instructions for citing data by submitting Data Collections to the ATLAS-D2K Data Explorer.

If you have any questions or feedback, please send them to your consortium's help email: [help@atlas-d2k.org](mailto:help@atlas-d2k.org).

**If you are creating a Collection for an upcoming paper, please make sure you are citing it correctly!** You may find citation instructions here: [https://www.atlas-d2k.org/citing/](https://www.atlas-d2k.org/citing/)

<!--
We also have the following training materials available:
* [Webinar Slides](https://docs.google.com/presentation/d/1cJBcdiuF67ze1qMSIOykghA569t8gdcALPRR22C5R7s/edit?usp=sharing)
* [Webinar Replay 02/08/2018 (17:06)](https://youtu.be/OCHq4GwzEFc)
-->
<a name="overview"/>

## Overview

Adding data Collections involves the following steps:

* Make sure you are in the correct Globus authentication group ([follow the instructions on this page](../accessing-atlas-resources/)), and that you are logged in.
* Create the base Collection record (contains the metadata).
* Then on the new Collection record, for each type of data you would like to include, scroll down to the appropriate section and add the data records you want to include.

## What is a Collection for?

A collection is useful anytime you want to group data under one DOI or citation. Some common use cases include:

* An upcoming publication
    * A collection can be properly cited in the paper
    * Data set citation (based on the [Nature scientific data citation format](http://blogs.nature.com/scientificdata/2016/07/14/data-citations-at-scientific-data))

    Example: **McMahon, A. GUDMAP Consortium. https://doi.org/10.25548/BURB-6P44  (2017)**

    * Readers can unambiguously obtain data referred in the paper → **repeatable experiments!**
* A published publication
    * A collection can refer to the published paper in its description.
    * Readers can unambiguously obtain data referred in the paper → **repeatable experiments!**
* Collaboration
    * Create a specific set of data to be used for further discussion or collaboration.


## 1. Create the base Collections record


* Go to [www.atlas-d2k.org](https://www.atlas-d2k.org/) and log in.
* On the top-level menu, click "*Internal*" and then choose "*Data Collections*" to go to the metadata entry form:
<!--
![Screenshot of the Create Collection Record form](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/collection-create-form-update.png)
-->
* Select the values for each relevant field. The required fields are:
  * _Title_
  * _Description_: Try to give a good description of what the data is related to (ie, "This collection includes the original images for figures in XYZ paper")
  * _Require DOI?_: Set this to **true** in order to generate a permanent identifier for this collection (Please set this to true for collections related to publications).
  * _Curation Status_:
      * While you're working on the record, choose either _In Preparation_ (still drafting).
      * When you are ready to submit to the ATLAS-D2K Center, change this to _Submitted_ and send email to the Center that it is ready for review at [help@atlas-d2k.org](mailto:help@atlas-d2k.org).
      * If you want to delay the release of the Collection (ie, until the related paper is published), change this field to _Embargoed_.
      * Your data will **not** be viewable publicly until approved for _Release_ by the Center. [For a complete description of the Curation Process, click here.](../curation-workflow/)
  * _Principal Investigator_: Choose the name of your project's contact PI.
  * _Data Provider_: Choose your institution.
  * _Consortium_: Make sure you indicate whether this is from the ATLAS-D2K consortium.
* Click _Save_ (scroll to the top of the page) to save the record.

**You can come back at any time and click "Edit" in the record header to modify this record.**

## 2. Add your data records

Once the base Collection record is created, now you can add the related data. To the left, you'll see a Sections list that will take you further down the page to sections for each type of data you can link.

**If you don't see a section for data you want to include, email [help@atlas-d2k.org](mailto:help@atlas-d2k.org).**
<!--
[![Screenshot of the Create Collection Record form](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/collections-record-blank-update.png)](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/collections-record-blank-update.png)
-->
* In each relevant section, click `+ Link records` to the right of the section header.

* Browse or search for the records you want to add and then click the checkboxes to select them.
<!--
![Screenshot of the Create Collection Record form](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/collection-record-blank-select-update.png)
-->
* Click _Save_ to add them to the Collection record.  

## 3. Reviewing and Submitting Data Collections

Here is how to find your project's data with a Curation Status of "In Preparation":

* Make sure you are logged in.

* Go to the [Collections search page](https://www.atlas-d2k.org/chaise/recordset/#2/Common:Collection).

* In the faceting sidebar on the left, choose the following filters:
    * Under **Curation Status**, choose _In Preparation_.
    * Under **Principal Investigator**, choose your project's PI. Now you should see the data you need to review.

* When your record is approved internally, change _Curation Status_ to _Submitted_ to send it to the Hub (click here for the full [Curation Workflow](/docs/curation-workflow)).

## 4. Deleting Data Collections

Before you can delete the base Collection record, you need to unlink any data records associated with it.

To delete a data collection record:

* Scroll down the record to the sections for the different data types that were linked to the Collection.

* In each of these sections, unlink the entries by clicking the 'x' icon in the _Actions_ columns.

* Once all of the related records have been unlinked (deleted), then scroll up to the top of the record and click _Delete_.
