---
title: Submitting Cell Lines
permalink: /docs/cell-lines/
---

<!-- uncomment when generating PDF in Atom
# Submitting Cell Lines
-->
<!-- comment out when generating PDF in Atom
**[PDF version](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Submitting-Cell-Lines.pdf)**
-->

This page provides instructions for submitting cell lines to the ATLAS-D2K Data Explorer.

If you have any questions or feedback, please send them to your consortium's help email: [help@atlas-d2k.org](mailto:help@atlas-d2k.org).

We also have the following training materials available:
<!--
* [Webinar Slides](/assets/slides/GUDMAP-RBK-02082018-data_submission_workshop-collections.pptx)
-->
* [Webinar Replay 02/08/2018 (17:06)](https://youtu.be/OCHq4GwzEFc)

<a name="overview"/>

## Overview

Adding cell lines involves the following steps:

* Make sure you are in the correct Globus authentication group ([follow the instructions on this page](accessing-gudmap-and-rbk-resources/)), and that you are logged in.
* Create the base Cell Line record.
* Then you will add related records (or tables) to the base record, including validation assets and reporter vector maps.

Note: Make sure the parental cell line is in the system (_Search > Cell &amp; Animal Models > Parental Cell Lines_). If it's not there, you will need to add it (see [Adding a Parental Cell Line](#adding-a-parental-cell-line)).

## Create base record

From anywhere within the ATLAS-D2K data repository, go to the top navigation bar and click _Create > Cell &amp; Animal Models > Reporter Cell Lines_. (You must be logged in.)

![Form to create the base record](/assets/wiki_images/submitting-data/cell-lines-base-create.png)

Tip: Enter as many fields as you can. The more fields you enter, the more details are available in the filter sidebar for users to search by.

All of the available fields are listed below and required fields are in **bold**:

* **Name**
* Gene
* Genotype
* Source Line
* **Parental Line**
* Reporter Category
* Donor Status
* Sex
* Organism
* Cell Line Type
* Reprogramming Method Reference
* Targeting Approach
* Reporter
* Cas9 Protospacer
* Pluripotency
* Karyotype
* Karyotype File	(Upload file)
* **Principal Investigator** - Note: Add the PI for your project. When you click the field, a modal window will open. If the name of your PI is not available, add them using "+" sign (Create new record) button.
* **Consortium**

Once you have entered your information, scroll back up to the top of the page and click "Submit". Your base record is now created.

## Add related records

Add related records in the following tables:

### Cell Type Marked

Click the `Add` link to the right of the table.

![Add Cell Type](/assets/wiki_images/submitting-data/cell-lines-types-add.png)

A new browser tab will open with the Create Record form.

![Form to create the cell type](/assets/wiki_images/submitting-data/cell-lines-types-create.png)

In the form, choose values for the following fields:

* Kidney Lineage
* Cell Type

If the value you need is not available, you can add it using the "+" plus sign button.

When you are finished, click the "Submit" button and close the browser tab.

###  Pluripotency, Reporter, Targeting Validation Asset Records

There are three types of validation asset records that you may link to this record: _pluripotency_, _report_ and _targeting_. For each of these, click the `Add` link.

![Add Validation asset record](/assets/wiki_images/submitting-data/cell-lines-validation-add.png)

A new browser tab will open with the Create Record form (using Pluripotency Validation Asset as an example).

![Create Validation asset record](/assets/wiki_images/submitting-data/cell-lines-validation-create.png)

In the form, enter the following fields.

* Validation Asset
* Asset Type	- Choose "microscopy" or "array".

Note that the last field is _Curation Status_. This field should be set initially to "Biocurator Review". Don't change this value. The biocurator will review this record and make sure it's correct.

Click the "Submit" button at the top of the page and then close the browser tab.

###  Reporter Vector Map

Towards the bottom of the page, you'll find the Reporter Vector Map section. Click the `Add` link.

![Add vector map record](/assets/wiki_images/submitting-data/cell-lines-vector-map-add.png)

A new browser tab opens with the Create Record form.

![Create vector map record](/assets/wiki_images/submitting-data/cell-lines-vector-map-create.png)

Select values for the following fields:

* Vector Map - If the system does not already include the Vector Map you need, use the "+" button to create a new value and then select it.
* Map Type

Note that the last field is _Curation Status_. This field should be set initially to "Biocurator Review". Don't change this value. The biocurator will review this record and make sure it's correct.

Click the "Submit" button at the top of the page and then close the browser tab.

## Adding a Parental Cell Line

If you do not see the parental cell line already in the system (by choosing _Search > Cell &amp; Animal Models > Parental Cell Lines_), you'll need to add it.

From the navigation bar, choose _Create > Cell &amp; Animal Models > Parental Cell Lines_. The Create Form for the parental cell line appears.

![Create parental cell line record](/assets/wiki_images/submitting-data/cell-lines-parental-create.png)

Tip: Fill out as many fields as you can. This improves the ability for users to find this record in the filtering sidebar or other methods of search.

The following are all of the fields available. Required fields are in **bold**.

* **Name**
* Organism
* Cell Line Type
* Transient Modification
* Donor Ethnicity
* Donor Stage
* Donor Sex
* Donor Age
* Pluripotency
* Germ Layer Staining
* Sequenced
* Tissue
* Organ
* Reference Source
* Precursor Cell Name
* Passage Number
* Cell Line Made At
* Kidney Organoids Status
* Comments - Optional text box if you want to add additional information.
* **Principal Investigator** - Note: Add the PI for your project. When you click the field, a modal window will open. If the name of your PI is not available, add them using "+" sign (Create new record) button.
* **Consortium**

When you are finished, click the "Submit" button at the top of the page.
