---
title: Submitting Specimen Data
permalink: /docs/specimen/
---

<!-- uncomment when generating PDF in Atom
# Submitting Specimen and Imaging Data (H&E, IF, ISH, etc)
-->
<!-- comment out when generating PDF in Atom
**[PDF version](../specimens/.pdf)**
-->

This page provides instructions for adding specimen and imaging data (such as histology, immunohistochemical, in situ hybridization images, etc) to the ATLAS-D2K Data Explorer.

If you have any questions or feedback, please send them to : [help@atlas-d2k.org](mailto:help@atlas-d2k.org).

## Related materials

- [Tutorial slides from 5/30/2019 - Model V2](raw/assets/slides/Specimen-Training-20190530-slides.pptx)
- [Webinar from 5/30/2019](https://youtu.be/J9v8N1brHcY)

## Overview of specimen data submission process

The following are the basic steps you’ll take to add specimen and imaging data. Note that you will see many other possible fields/tables you can add and the more information you provide, the more discoverable is your data.

The following are the minimum requirements:

- [Overview of specimen data submission process](#overview-of-specimen-data-submission-process)
- [1. Join the Globus group.](#1-join-the-globus-group)
- [2. Create a **Specimen** record](#2-create-a-specimen-record)
  - [Tips for navigating the base Specimen record](#tips-for-navigating-the-base-specimen-record)
- [3. Add the Anatomical Source](#3-add-the-anatomical-source)
  - [3.1. To add the same anatomical source to several Specimen records](#31-to-add-the-same-anatomical-source-to-several-specimen-records)
- [Add related records](#add-related-records)
- [4. Add at least one imaging data record](#4-add-at-least-one-imaging-data-record)
  - [4.1. Processing CZI files](#41-processing-czi-files)
  - [Batch Add Image Records](#batch-add-image-records)
- [5. Add an Antibody record if an antibody was used to stain the slide](#5-add-an-antibody-record-if-an-antibody-was-used-to-stain-the-slide)
- [6. Add Specimen Probe Association if a probe was used to probe for a gene](#6-add-specimen-probe-association-if-a-probe-was-used-to-probe-for-a-gene)
- [7. Add Specimen Expression record if gene expression was scored](#7-add-specimen-expression-record-if-gene-expression-was-scored)
- [8. Stages/Timing for Human Organoid Specimens](#8-stagestiming-for-human-organoid-specimens)
- [9. Submit and Releasing your Data](#9-submitting-your-data-for-review-and-release)

Here are the details for each step.

## 1. Join the Globus group.

* You will need to be in the appropriate Globus group for editing access. Please email the ATLAS-D2K Center at [help@atlas-d2k.org](mailto:help@atlas-d2k.org) to ask for help joining the correct group. For more information, see [Accessing ATLAS-D2K Resources](../accessing-atlas-resources/).



## 2. Create a **Specimen** record

The first thing you’ll do is create the base metadata record which describes the Specimen (slide). A specimen is a unit of tissue from a single organism (person/mouse/zebrafish).

Once you create this, then you’ll add the Specimen data (ie, upload image files) and link it to this record.

Make sure you are logged in.

**Step 1:** Go to a [_Specimen_](https://www.atlas-d2k.org/chaise/recordset/#2/Gene_Expression:Specimen@sort(RCT::desc::,Stage_Ordinal,RID)) page and log in.

**Step 2:** Click the **Create** button.

[![Screenshot of the Create button](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-create-record-sm.png)](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-create-record.png)

**Step 3:** Fill out the form fields.

There are a few fields that are required or you may not save the form (these are indicated with the red asterisk *).

However, we recommend filling in as many fields as possible. **The more fields you fill out the more ways users can find your data**. For example, if you include the age stage and sex, then this data will show up for Specimen searches for that specific age stage and sex.

Recommended fields: click the dropdown field and choose the appropriate value:

* **Species**: e.g., *Homo sapiens*, *Mus musculus*.

* **Assay type**: The imaging related types are *IHC*, *ISH*, and *Histology*.

* **Stage**: The Theiler or Carnegie stage (preferred). If you cannot provide the stage, there is also the **Chronological Age** field where you can type in the age using free text.

* **Sex**: *Male*, *Female*, *Unknown* or *Both*.

* Describe how the sample was prepared with the following fields:

    * **Preparation**

    * **Fixation**

    * **Embedding**

* **Curation Status**: The default value is *In Preparation* which means this record is in draft mode and will only be viewable by other Consortium members who are logged in. *PI Review* is also available if your internal process would like to indicate records ready for the PI to review. Once you are finished, update this field to *Submitted* to send to the Hub for further curation. The biocurator may contact you with further questions about the data before it is released. For more information, see [Curation Workflow](../curation-workflow/)

* **Principal Investigator**: Choose the appropriate Principal Investigator. If your PI is not on the list, click the plus sign just to the top right of the list to create a new record for them.

* **Consortium**.

These fields may be useful:

* **Internal ID**: A useful field for your own lab’s tracking purposes.

* Information about the organism:

    * **Strain**

    * **Wild Type**

    * **Phenotype**

    * **Cell Line**

* Descriptive fields:

    * **Upload Notes**

    * **Probe Usage Notes**

* **Parent Specimen:** If you have subdivided a biological sample (created sections from a sample), you can create a Specimen record for the original sample and designate it as the "parent" of the Specimen records for all the subdivided samples. You can continue doing this to show different levels of grandparent/parent/child relationships.

* **Representative Image**: This is an optional thumbnail of the image. If you do not add one, the system will automatically select the thumbnail from the first image record. [Read this doc for our thumbnail guidelines.](../thumbnail-creation-guideline/)

Once you have filled out the fields, click the **Save** button at the top of the form to save the record.

You have now created the basic Specimen record. But there's still some more data to add.

## 3. Add the Anatomical Source

From the Specimen record, add at least one *Anatomical Source*. In the summary section towards the top of the page, look for "Anatomical Source" and click the link. To the right of page, click the `Add record` button. Start typing a term and choose your term from the list of available ontological terms, then click **Submit**.

[![Screenshot of the Add button for ](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-anatomical-source.png)](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-anatomical-source.png)

* To indicate stem cell lines, search for iPSC or hiPSC.
* You may enter more than one anatomical source, for example, if you entered iPSC or hiPSC, add another anatomical source and search for "podocyte", "kidney organoid", etc.
* To enter the cell line, click "Edit" for the Specimen record, scroll down to the Cell Line field and click the dropdown field to show available lines. Search for the cell line. If it is not available, you can click "Create new", fill in the form and click "Submit" to add it to the list.

### 3.1. To add the same anatomical source to several Specimen records

This is a great shortcut **if you have many Specimen records that you want to add the same Anatomical Source**. You can do an anatomy search for the term and then link multiple Specimen records to it:

1. Go to [Anatomy Facet Search](https://www.atlas-d2k.org/chaise/recordset/#2/Vocabulary:Anatomy/).
2. Search or filter to find the anatomical term you need and click its eye icon.
3. Click `Specimens` in the left Sections sidebar or scroll down to that section, then click `Add` to the right of the table.
4. In this window, you can filter or search for your Specimen records, select the ones you want to associate with this anatomical term, and click `Submit`.

## Add related records

You'll notice that on your Specimen record, after the initial list of metadata you added, there are many other sections underneath. These allow you to add data files and information related to this Specimen record. The following are required:

* **For all imaging data types**, you must add at least one `Image` record.
* **If an antibody was used to stain the slide**, add an `Antibody` record.
* **If a probe was used to probe for a gene**, add a `Probe` record.
* **If you examined the slide and scored expression values (_present, not present_, etc.) for a gene**, add `Specimen Expression` records.

The following sections describe how to add these types of records.

## 4. Add at least one Image, Image 3D or Video record

The system will accept images (2D and 3D) and videos. Please consult the following lists of accepted file formats and video platforms: [Standard file formats for data submission](../standard-files-and-formats-for-submission/) and [Available Video Platforms](../available-video-platforms/)).

**Note:** these instructions specify how to add `Image` records on the ATLAS-D2K website. If you have many image files, you may also [upload them using our bulk-upload client tool](../bulk-uploading-image-files/).

Go to the **Image** section (for 2-D files), **Image 3D** section (for 3-D files), or **Video** section (for videos) and click the `Add record` button to the right.

[![Screenshot of the Add button for ](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-new-image-sm.png)](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-new-image.png)

This will open a form in a new browser tab.

[![Screenshot of Create Image form](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-create-image-form-sm.png)](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-create-image-form.png)

Fill out the fields on this form. Use the **Original File** field to upload your data file and click `Save` to save the record.

We also recommend adding a thumbnail for this record. [Read this doc for our thumbnail guidelines.](../thumbnail-creation-guideline/).

### 4.1. Processing CZI files

Where applicable, we encourage submitting CZI files. The system will convert CZI files for in-browser viewing. This may take a few hours but it will automatically appear once they have been converted.

The browser will allow the user to manipulate channels and zoom in to see details in high resolution.

### 4.2 Batch Add Image Records

If uploading more than one image record, you may click the `Clone` button to open multiple records.

[![Screenshot of the Clone button](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-clone-button-sm.png)](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-clone-button.png)

[![Screenshot of examples of cloned forms](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-clone-example-sm.png)](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-clone-example.png)

**Tip:** If you are using similar field values - fill in the values of the field before you click the plus sign and those values will propagate to the cloned record forms.

If you decide you do not want one of the records, just click the `X` icon to delete.

When you are finished, click **Save** to save the record.

## 5. Add an Antibody record if an antibody was used to stain the slide

Go to the *Specimen Antibody* table and click `Add record` to add an antibody.

[![Screenshot of examples of cloned forms](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-antibody-record-sm.png)](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-antibody-record.png)

The *Create New Specimen Antibody* form appears.

Many of the fields on this page are automatically generated. The important thing to fill out here is the *Antibody RID* to indicate the company. Click the field to see a list of existing companies in the catalog.

If you do not see the antibody company listed, click the **Create New** button to add it.

[![Screenshot of Create New button when you open Antibody RID field](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-antibody-rid-create-new-sm.png)](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-antibody-rid-create-new.png)

## 6. Add Specimen Probe Association if a probe was used to probe for a gene

If you want to associate one or more genes with this specimen, you’ll need to populate the *Specimen Probe Association* table. In the following screenshot, two tables are highlighted. Specimen Probe Association is where you will associate the probe(s) with the data. The *Probe* table will display details of the probe(s) you chose - you do not manually add anything to this table.

Go to the *Specimen Probe Association* section and click the `Add record` link.

[![Screenshot of Add Record in the Specimen Probe Association section](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-probe-association-sm.png)](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-probe-association.png)

Here is how it looks after adding a probe to the Specimen Association Table:

[![Screenshot of example of new probe record](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-probe-example-sm.png)](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-probe-example.png)

## 7. Add Specimen Expression record if gene expression was scored

For In Situ Hybridization data, you’ll also add scored expression regions.

Go to the *Specimen Expression* table and click `Add record`.

[![Screenshot of example of new probe record](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-expression-record-sm.png)](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-expression-record.png)

The *Create new Record: Specimen Expression* form appears. There are various descriptive fields you may fill out, but at the very least, you’ll need to indicate the anatomical region and its expression score (the strength of expression in that region).

[![Screenshot of the fields for "Expression Region" and "Strength"](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-expression-scored-sm.png)](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-expression-scored.png)

Click the `Expression Region` field to choose the anatomical region.

Click the `Strength` field to choose from *uncertain*, *present*, and *not detected*.

The click **Save** to save the Specimen Expression record.

## 8. Stages/Timing for Human Organoid Specimens

Kidney organoids are derived from pluripotent stems cells (ESC or iPSC) using a variety of possible protocols. To help standardize assignment of stages of organoid development, we will adopt the convention found in the published literature. This defines the onset of induction as Day 0.

- Day 0 = Induction of iPSCs or ESCs to begin differentiation (i.e. CHIR99021 added)

Each protocol may vary in the rate of formation subsequent to induction, thus the protocol used for a given experiment must be clearly documented with an entered specimen. This can be a reference to a protocol in the GUDMAP database, or the published paper that details the approach (include PMCID/PMID number).


**REFERENCES:**

>Takasato M, Er PX, Chiu HS, Maier B, Baillie GJ, Ferguson C, Parton RG, Wolvetang EJ, Roost MS, Chuva de Sousa Lopes SM, Little MH, 2015. Kidney organoids from human iPS cells contain multiple lineages and model human nephrogenesis. Nature 526, 564–568. PMID: 26444236

>Morizane R, Lam AQ, Freedman BS, Kishi S, Valerius MT, Bonventre JV, 2015. Nephron organoids derived from human pluripotent stem cells model kidney development and injury. Nat Biotechnol 33, 1193–1200. PMCID: PMC4747858

## 9. Submitting Your Data for Review and Release

Once you have completed the record and any internal review and are ready to submit to the Hub, edit the Specimen base record.

[![Screenshot of where to find the Edit button](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-record-edit-sm.png)](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-record-edit.png)

Scroll down to the *Curation Status* field and change the status to *Submitted*. Then click the **Save** button to save the record.

This record will then go to **Biocuration Review** and the biocurator may contact you to clarify something or to correct an aspect of the data before they update the status to **Released**. Only at this point can the public view the data.