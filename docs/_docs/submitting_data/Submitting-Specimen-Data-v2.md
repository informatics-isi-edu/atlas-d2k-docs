---
title: Submitting Specimen Data - rewrite
permalink: /docs/specimen-v2/
---

This guide will walk you through the steps to submit specimen and imaging data to the ATLAS-D2K Data Explorer. If you have any queries, please reach out to [help@atlas-d2k.org](mailto:help@atlas-d2k.org).

## Table of Contents

- [Overview](#overview-of-the-submission-process)
- [1. Joining the Globus Group](#1-joining-the-globus-group)
- [2. Creating a Specimen Record](#2-creating-a-specimen-record)
- [3. Adding the Anatomical Source](#3-adding-the-anatomical-source)
  - [3.1. Adding Anatomical Source to Multiple Records](#31-to-add-the-same-anatomical-source-to-several-specimen-records)
- [4. Uploading Image Records](#4-upload-image-records)
  - [4.1. CZI File Processing](#41-processing-czi-files)
  - [4.2. Batch Upload Image Records](#42-batch-add-image-records)
- [5. Incorporating Antibody Data](#5-add-an-antibody-record)
- [6. Associating Probes to Genes](#6-add-specimen-probe-association)
- [7. Documenting Gene Expression Scores](#7-add-specimen-expression-record)
- [8. Documenting Stages for Human Organoids](#8-stagestiming-for-human-organoid-specimens)
- [9. Finalizing Your Submission](#9-submitting-your-data-for-review-and-release)

## Overview of the Submission Process

Follow the steps outlined to enhance the discoverability of your specimen and imaging data. The more details you provide, greater is the ease of discovery.

## 1. Joining the Globus Group

To get editing access, join the relevant Globus group. Email [help@atlas-d2k.org](mailto:help@atlas-d2k.org) for assistance. For detailed information, see [Accessing ATLAS-D2K Resources](../accessing-gudmap-and-rbk-resources/).

## 2. Creating a Specimen Record

A specimen refers to tissue from an organism like humans, mice, or zebrafish. Begin by creating its metadata record. Once done, upload the image files and link them.

- [Log in and create a Specimen](https://www.atlas-d2k.org/chaise/recordset/#2/Gene_Expression:Specimen@sort(RCT::desc::,Stage_Ordinal,RID)).
- Fill out the essential fields marked with a red asterisk (*). However, providing more details enhances data discoverability.
- Upon completion, save the record.

### 2.1 Field descriptions

The following are required fields:

| Field                 | Description                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Species**           | e.g., *Homo sapiens*, *Mus musculus*.                                                                                                                                                                                                                                                                                                                                   |
| **Assay type**        | The imaging related types are *IHC*, *ISH*, and *Histology*.                                                                                                                                                                                                                                                                                                            |
| **Curation Status**   | The default value is *In Preparation* which means this record is in draft mode and will only be viewable by other Consortium members who are logged in. For more information, see [Curation Workflow](../curation-workflow/). |
| **Principal Investigator** | Choose the appropriate Principal Investigator. If your PI is not on the list, click the plus sign just to the top right of the list to create a new record for them.                                                                                                                                                                                             |
| **Consortium**        |                      Select *GUDMAP* or *RBK*.                                                                                                                                                                                                                                                                                                                                                   |

The following fields are especially helpful for bringing up your data in search results:

| Field                 | Description                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Stage**             | The Theiler or Carnegie stage. If you cannot provide the stage, there is also the **Chronological Age** field where you can type in the age using free text.                                                                                                                                                                                              |
| **Sex**               | *Male*, *Female*, *Unknown* or *Both*.                                                                                                                                                                                                                                                                                                                                  |
| **Preparation**, **Fixation** and **Embedding** | These fields describe how the sample was prepared.                                                                                                                                                                                                                                                            |

| **Internal ID**       | A useful field for your own lab’s tracking purposes. This can be very useful to help you search for your Specimen records later.                                                                                                                                                                                                                                       |
| **Strain**, **Wild Type**, **Phenotype**, **Cell Line**     | Use these fields to provide helpful information about the specimen.                                                                                                                                                                                                                                                                               |
| **Upload Notes**, **Probe Usage Notes** | These fields are an opportunity to provide more context about the data.                                                                                                                                                                                                                                                                                                                               |
| **Parent Specimen**   | If you have subdivided a biological sample (e.g., you created sections from a sample), you can create a Specimen record for the original sample. Then for each section (child), designate the original sample as the "parent". You can continue doing this to show different levels of grandparent/parent/child relationships.                                             |
| **Representative Image** | This is an optional thumbnail of the image. If you do not add one, the system will automatically select the thumbnail from the first image record. [Read this doc for our thumbnail guidelines.](../thumbnail-creation-guideline/)                                                                                                                         |



## 3. Adding the Anatomical Source

From the Specimen record, add at least one *Anatomical Source* from our list of ontology terms. [You can also add specific cell lines or other sources.]

[To find the *Anatomical Source* field, look for the link on the left-hand Summary.]

### 3.1. To Add the Same Anatomical Source to Several Specimen Records

This shortcut is handy if many Specimen records require the same Anatomical Source.

- Navigate to [Anatomy Facet Search](https://www.atlas-d2k.org/chaise/recordset/#2/Vocabulary:Anatomy/).
- Find the required anatomical term and click View Details icon to open the page.
- Scroll down to the *Specimen* section and click `Link records` to link multiple Specimen records.

## 4. Upload Image Records

You can upload 2D images, 3D images, or videos. Check the accepted [file formats](../standard-files-and-formats-for-submission/) and [video platforms](../available-video-platforms/).

Go to the **Image** section for 2-D files, **Image 3D** section for 3-D files, or **Video** section for videos and click the `Add record` button to the right fill out the fields.

We highly recommend uploading a thumbnail file for the **Image** and **Image 3D** records. [Read this doc for our thumbnail guidelines.](../thumbnail-creation-guideline/).

### 4.1. Processing CZI Files

Submit CZI files if possible. These files get converted for in-browser viewing, allowing detailed insights.

### 4.2. Batch Add Image Records

You can upload multiple image records simultaneously, making the process efficient and faster.

[add details]

## 5. Add an Antibody Record

If the slide was stained with an antibody, it's essential to record this data.

## 6. Add Specimen Probe Association

For associating genes with specimens, populate the Specimen Probe Association table.

## 7. Add Specimen Expression Record

For In Situ Hybridization data, make sure to add scored expression regions.

## 8. Stages/Timing for Human Organoid Specimens

Documenting the organoid development stages ensures data uniformity and comprehension.

**REFERENCES:**

>Takasato M, Er PX, Chiu HS, Maier B, Baillie GJ, Ferguson C, Parton RG, Wolvetang EJ, Roost MS, Chuva de Sousa Lopes SM, Little MH, 2015. Kidney organoids from human iPS cells contain multiple lineages and model human nephrogenesis. Nature 526, 564–568. PMID: 26444236

>Morizane R, Lam AQ, Freedman BS, Kishi S, Valerius MT, Bonventre JV, 2015. Nephron organoids derived from human pluripotent stem cells model kidney development and injury. Nat Biotechnol 33, 1193–1200. PMCID: PMC4747858

## 9. Submitting Your Data for Review and Release

Upon finalizing your records and internal reviews, submit them to the Hub by changing the *Curation Status* field to *Submitted*.

The biocurator will review your submission and may have more questions for improving the quality of your submission.

Once the biocurator and submitter are satisfied that the data is complete, the biocurator will change the *Curation Status* field to *Release*, at which time it becomes publicly accessible.
