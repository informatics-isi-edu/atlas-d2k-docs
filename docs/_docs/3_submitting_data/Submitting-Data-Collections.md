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

## Table of Contents

TBD

## 1. Joining the Globus Group

To get editing access, join the relevant Globus group and make sure you are logged in. Email [help@atlas-d2k.org](mailto:help@atlas-d2k.org) for assistance. For detailed information, see [Accessing ATLAS-D2K Resources](../accessing-atlas-resources/).

## 2. What is a Collection?

In the ATLAS-D2K Center, we use the Collection to gather various data types together. One of the major characteristics of a Collection is that it can have a DOI assigned to it. A Collection is useful anytime you want to group data under one DOI or citation.

Some common use cases include:

* An upcoming publication
    * A collection can be properly cited in the paper
    * Here is an example of citing a collection (format is based on the [Nature scientific data citation format](http://blogs.nature.com/scientificdata/2016/07/14/data-citations-at-scientific-data))

    Example: **McMahon, A. GUDMAP Consortium. https://doi.org/10.25548/BURB-6P44  (2017)**

    * Readers can unambiguously obtain data referred in the paper → **repeatable experiments!**
* A published publication
    * A collection can refer to the published paper in its description.
    * Readers can unambiguously obtain data referred in the paper → **repeatable experiments!**
* Collaboration
    * Create a specific set of data to be used for further discussion or collaboration.

### 2.1 Overview for creating a Collection

Adding data Collections involves the following steps:

* [**Submit metadata**](#). When you first create a Collection record, you will fill out a form to submit metadata about the data described by this Collection.

* [**Link to your publication**](#).

* [**Link to protocols and contributors**](#). To provide more complete transparency, reproducibility and provenance, you will link to the protocols used to capture the data in this collection and document the people who handled the data.

* [**Link the data records**](#). This is where you connect the Collection to the data records you are organizing.


## 3. Submit Metadata Fields

* [Use this link to log in and create a Collection](https://staging.atlas-d2k.org/chaise/recordedit/#2/Common:Collection?pcid=navbar/recordedit&ppid=22tx2me522k42d4f1ung2rpx). Alternatively, from atlas-d2k.org,:
    - In the top-level menu, click *Internal*, then *Data Collections*.
    - From a "Collection" page, you can also click the `Create` button (you must be logged in to see this button).

* At a minimum, fill out the essential fields marked with a red asterisk (*). However, filling out more fields enhances data discoverability.

* Upon completion, click `Save`.

![Screenshot of the Create Collection form]({{ "/assets/wiki_images/submitting-data/TBD.png" | relative_url }})

### 3.1. Fields for Collection Metadata

| Field                  | Description                                                                                                                                                                                                                       | Required or Optional |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| Title                  | Provide the title of the Collection (this could be the title of your publication)                                                                                                                                                 | Required             |
| Description            | Provide a useful description of the Collection (for example this could be the abstract of your publication)                                                                                                                       | Required             |
| Details                | Use this field if there are other details you'd like to include.                                                                                                                                                                  | Optional             |
| Require DOI?           | This indicates to the Hub to generate a DOI for this Collection. Highly recommended for citing in your publication.                                                                                                               | Optional             |
| Curation Status        | Indicates if this record is still being worked on, is being reviewed, is embargoed until publication or has been released to the public. For a complete description of the Curation Process, click here.](../curation-workflow/)  | Required             |
| Principal Investigator | Use the primary Principal Investigator for this collection of data. You may only indicate one PI.                                                                                                                                 | Required             |
| Data Provider          | Use the institution of the Principle Investigator.                                                                                                                                                                                | Required             |
| Consortium             | Indicate the Consortium (GUDMAP, RBK, etc).                                                                                                                                                                                       | Required             |

Once you have saved the form, you will see a new Collection record much like the following example:

![Screenshot of a Specimen record]({{ "/assets/wiki_images/submitting-data/TBD.png" | relative_url }})

**You can come back at any time and click "Edit" in the record header to modify this record.**

## 4. Link to Publications

From the Collection record, link to the related publication. In the **Publication** field, click the `Link records` button.

If you know your publication has already been entered, search for the title and then click to link to the publication.

Otherwise, click the `Create new` button and fill out the fields with information about the publication. Click `Save` when you are finished.

### 4.1 Fields for Publication Records:

TBD

## 5. Provide Protocols and Contributors

After you've made the base Collections record, two other fields will appear: Protocols and Contributors. It's important to include this information for letting users know how specimen were processed and who conducted the protocols.

### 5.1 Link to Protocols

In the **Protocols** field, click `Link records` (one of the buttons on the right side of the screen).

A modal window will appear where you can search for an existing protocol in our database or click `Create new` to add a new protocol.

### 5.2 Add Contributors

In the **Contributors** field, click `Add records` (one of the buttons on the right side of the screen).

## 6. Link to your data records

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
