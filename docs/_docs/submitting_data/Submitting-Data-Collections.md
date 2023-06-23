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

If you have any questions or feedback, please send them to your consortium's help email: [help@gudmap.org](mailto:help@gudmap.org) or [help@rebuildingakidney.org](mailto:help@rebuildingakidney.org)

**If you are creating a Collection for an upcoming paper, please make sure you are citing it correctly!** You may find citation instructions here: https://www.rebuildingakidney.org/about/usage.html#citing-data-associated-with-a-publication

We also have the following training materials available:
* [Webinar Slides](https://docs.google.com/presentation/d/1cJBcdiuF67ze1qMSIOykghA569t8gdcALPRR22C5R7s/edit?usp=sharing)
* [Webinar Replay 02/08/2018 (17:06)](https://youtu.be/OCHq4GwzEFc)

<a name="overview"/>

## Overview

Adding data Collections involves the following steps:

* Make sure you are in the correct Globus authentication group, [kidney-writers](/docs/protocols#1-join-the-kidney-writers-group), and that you are **logged in**.
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
<!--
## Permanent ID (DOI)

* Digital Object Identifier (DOI)
    * DOI: 10.25548/BURB-6P44
    * DOI URL: https://doi.org/10.25548/BURB-6P44
* DOI issuance process
    * The collection metadata (Title, Description, PI, Consortium) is registered with the DOI registry which  means your data set is searchable no matter if the website URL changes.
    * The collection URL (our permalink URL) is registered with the DOI.   
* When is a DOI issued? When
    * _Require DOI?_ field equals "true"; and
    * _Curation Status_ field equals "Released"
    -->

<div class="page-break"></div>

## 1. Create the base Collections record

* Go to the Collection page and click the "Create" button:

![Screenshot of the Create Collection Record form](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/collection-create-update.png)

  The `Create new Collection` form appears in a new browser tab.

  ![Screenshot of the Create Collection Record form](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/collection-create-form-update.png)


* Select the values for each relevant field. The required fields are:
  * _Title_
  * _Description_: Try to give a good description of what the data is related to (ie, "This collection includes the original images for figures in XYZ paper")
  * _Require DOI?_: Set this to **true** in order to generate a permanent identifier for this collection (Please set this to true for collections related to publications).
  * _Curation Status_:
      * While you're working on the record, choose either _In Preparation_ (still drafting) or _PI Review_ (if your lab wants to indicate the PI should review it).
      * When you are ready to submit to the Hub, change this to _Submitted_ and send email to the Hub that it is ready for review.
      * If you want to delay release of the Collection (ie, until the related paper is published), change this to _Embargoed_.
      * Your data will **not** be viewable publicly until approved for _Release_ by the Hub. [For a complete description of the Curation Process, click here.](/docs/curation-workflow)
  * _Principal Investigator_: Choose the name of your project's contact PI.
  * _Data Provider_: Choose your institution.
  * _Consortium_: Make sure you indicate whether this is from the ATLAS-D2K consortium.
* Click _Save_ (scroll to the top of the page) to save the record.

**You can come back at any time and click "Edit" in the record header to modify this record.**

<div class="page-break"></div>

## 2. Add your data records

Once the base Collection record is created, now you can add the related data. To the left, you'll see a Sections list that will take you further down the page to sections for each type of data you can link.

**If you don't see a section for data you want to include, email [help@gudmap.org](help@gudmap.org) or [help@rebuildingakidney.org](help@rebuildingakidney.org).**

[![Screenshot of the Create Collection Record form](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/collections-record-blank-update.png)](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/collections-record-blank-update.png)

* In each relevant section, click `Add record` to the right of the section header.

* Browse or search for the records you want to add and then click the checkboxes to select them.

![Screenshot of the Create Collection Record form](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/collection-record-blank-select-update.png)

* Click _Save_ to add them to the Collection record.  

<div class="page-break"></div>

## 3. Reviewing and Submitting Data Collections

Here is how to find your project's data with a Curation Status of "In Preparation" or "PI Review"**

* Make sure you are logged in.

* Go to the [Collections search page](https://www.gudmap.org/chaise/record/#2/Common:Collection/).

* In the faceting sidebar on the left, choose the following filters:
    * Under **Curation Status**, choose _PI Review_ and _In Preparation_.
    * Under **Principal Investigator**, choose your project's PI. Now you should see the data you need to review.

* When your record is approved internally, change _Curation Status_ to _Submitted_ to send it to the Hub (click here for the full [Curation Workflow](/docs/curation-workflow)).


<div class="page-break"></div>

## 4. Deleting Data Collections

Before you can delete the base Collection record, you need to unlink (delete) any data records associated with it.

To delete a data collection record:

* Scroll down the record to the sections for the different data types.

* In each of these sections, unlink the entries by clicking the 'x' icon in the _Actions_ columns.

* Once all of the related records have been unlinked (deleted), then scroll up to the top of the record and click _Delete_.
