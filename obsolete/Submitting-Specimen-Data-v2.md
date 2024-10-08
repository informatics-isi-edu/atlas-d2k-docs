---
title: Submitting Specimen Data - updated
permalink: /docs/specimen-v2/
---

This guide will walk you through the steps to submit specimen and imaging data to the ATLAS-D2K Data Explorer. If you have any queries, please reach out to [help@atlas-d2k.org](mailto:help@atlas-d2k.org).

## Table of Contents

- [Metadata Model for Specimen Records](#metadata-model-for-specimen-records)
- [1. Joining the Globus Group](#1-joining-the-globus-group)
- [2. Creating a Specimen Record](#2-creating-a-specimen-record)
- [3. Adding the Anatomical Source](#3-adding-the-anatomical-source)
  - [3.1. Adding Anatomical Source to Multiple Records](#31-to-add-the-same-anatomical-source-to-several-specimen-records)
- [4. Uploading Image Records](#4-upload-image-records)
  - [4.1. CZI File Processing](#41-processing-czi-files)
  - [4.2. Batch Upload Image Records](#42-batch-upload-image-records)
    - [4.2.1 Clone Records](#421-clone-records)
    - [4.2.2. Use DERIVA Client Tools](#422-use-deriva-client-tools)
- [5. Adding a new Human Reference Atlas (HRA) 3D coordinate](#5-adding-a-new-human-reference-atlas-hra-3d-coordinate)
  - [5.1 Editing an existing HRA 3D coordinate](#51-editing-an-existing-hra-3d-coordinate)
- [6. Adding an Antibody Record](#6-adding-an-antibody-record)
- [7. Associating Probes to Genes](#7-associating-probes-to-genes)
- [8. Documenting Gene Expression Scores](#8-documenting-gene-expression-scores)
- [9. Documenting Stages for Human Organoids](#9-documenting-stages-for-human-organoids)
- [10. Finalizing Your Submission](#10-submitting-your-data-for-review-and-release)


Follow the steps outlined to enhance the discoverability of your specimen and imaging data. The more details you provide, the greater is the ease of discovery.

## Metadata Model for Specimen Records

![Chart of Data Model for Specimen records]({{ "/assets/wiki_images/submitting-data/ATLAS_Data_Model_Specimen.jpg" | relative_url }})

## 1. Joining the Globus Group

To get editing access, join the relevant Globus group. Email [help@atlas-d2k.org](mailto:help@atlas-d2k.org) for assistance. For detailed information, see [Accessing ATLAS-D2K Resources](../accessing-atlas-resources/).

## 2. Creating a Specimen Record

A specimen refers to tissue from an organism like humans, mice, or zebrafish. Begin by creating its metadata record. Once done, upload the image files and link them.

- [Log in and create a Specimen](https://www.atlas-d2k.org/chaise/recordset/#2/Gene_Expression:Specimen@sort(RCT::desc::,Stage_Ordinal,RID)).
- Fill out the essential fields marked with a red asterisk (*). However, providing more details enhances data discoverability.
- Upon completion, save the record.

Alternatively, you can create specimen records using a CSV file or spreadsheet. See [Adding specimen records from a file](../adding-specimen-records-from-a-file/) for more details.

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

| **Internal ID**       | An important field for your own lab’s tracking purposes. This can be very useful to help you search for your Specimen records later and is critical if [using the DERIVA client tools](../bulk-upload-with-deriva-client-tools/) to bulk upload data.                                                                                                                |
| **Strain**, **Wild Type**, **Phenotype**, **Cell Line**     | Use these fields to provide helpful information about the specimen.                                                                                                                                                                                                                                                                               |
| **Upload Notes**, **Probe Usage Notes** | These fields are an opportunity to provide more context about the data.                                                                                                                                                                                                                                                                                                                               |
| **Parent Specimen**   | If you have subdivided a biological sample (e.g., you created sections from a sample), you can create a Specimen record for the original sample. Then for each section (child), designate the original sample as the "parent". You can continue doing this to show different levels of grandparent/parent/child relationships.                                             |
| **Representative Image** | This is an optional thumbnail of the image. If you do not add one, the system will automatically select the thumbnail from the first image record. [Read this doc for our thumbnail guidelines.](../thumbnail-creation-guideline/)                                                                                                                         |



## 3. Adding the Anatomical Source

From the Specimen record, add at least one *Anatomical Source* from our list of ontology terms.

[![Chart of data model](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-anatomical-source.png)](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-anatomical-source.png)

In the summary section towards the top of the page, look for "Anatomical Source" and click the link. To the right of page, click the `Add record` button. Start typing a term and choose your term from the list of available ontological terms.

* To indicate stem cell lines, search for `iPSC` or `hiPSC`.
* You may enter more than one anatomical source, for example, if you entered iPSC or hiPSC, add another anatomical source and search for "podocyte", "kidney organoid", etc.
* To enter the cell line, click "Edit" for the Specimen record, scroll down to the Cell Line field and click the dropdown field to show available lines. Search for the cell line. If it is not available, you can click "Create new", fill in the form and click "Submit" to add it to the list.


### 3.1. To Add the Same Anatomical Source to Several Specimen Records

This shortcut is handy if many Specimen records require the same Anatomical Source.

- Navigate to [Anatomy Facet Search](https://www.atlas-d2k.org/chaise/recordset/#2/Vocabulary:Anatomy/).
- Find the required anatomical term and click View Details icon to open the page.
- Scroll down to the *Specimen* section and click `Link records` to link multiple Specimen records.

## 4. Upload Image Records

You can upload 2D images, 3D images, or videos. Check the accepted [file formats](../standard-files-and-formats-for-submission/) and [video platforms](../available-video-platforms/).

Go to the **Image** section for 2-D files, **Image 3D** section for 3-D files, or **Video** section for videos and click the `Add record` button to the right and fill out the fields.

We highly recommend uploading a thumbnail file for the **Image** and **Image 3D** records. [Read this doc for our thumbnail guidelines.](../thumbnail-creation-guideline/).

### 4.1. Processing CZI Files

Submit CZI files if possible. These files get converted for in-browser viewing, allowing detailed insights. The browser will allow the user to manipulate channels and zoom in to see details in high resolution.

### 4.2. Batch Upload Image Records

#### 4.2.1. Clone Records

If you need to upload multiple image records simultaneously through the web interface, use the `Clone` button:

- Fill in the values of the field in the form that will be common across multiple records.
- Click the `Clone` button to create additional forms and edit individual ones as needed.

#### 4.2.2. Use DERIVA Client Tools

If you have many files or your files are very large (over 5GB), then you may need to use our client tools for uploading files programmatically. See [Bulk Uploading Image Files](../bulk-uploading-image-files/) for more details.

## 5. Adding a new Human Reference Atlas (HRA) 3D coordinate

If your specimen record is for human data, please use the following directions to register it with HuBMAP's RUI tool integrated into ATLAS-D2K. The Registration User Interface (RUI) supports spatially registering human tissue blocks to a 3D reference organ in the HRA using the Common Coordinate Framework (CCF) Registration User Interface (RUI) from HuBMAP.

You can find the [**video tutorial** for using this tool here](https://www.youtube.com/watch?v=gY3_-LIoKaU).

![Linking accounts page]({{ "/assets/img/rui-start-registration.jpg" | relative_url }})
_The "Start registration" page_

![Linking accounts page]({{ "/assets/img/rui-registration-interface.jpg" | relative_url }})
_The main RUI registration interface_

1. With your Specimen record in edit mode, scroll down to find the _HRA 3D Coordinate_ field and click "Select a value" to choose an “HRA 3D Coordinate”.
2. Click the _Create new_ button on the top right of the table.
3. In the "Name" field, add a logical name for the coordinate.
4. Click "Select a value" in the Registration UI field to open the **CCF-RUI** tool.
5. Fill in the fields and click "Start Registration".
6. Enter the values in the RUI tool: set the Anatomical Structure, and indicate the location of the sample by dragging the square into the correct location of the organ. The RUI interface offers two ways of navigation: 2D (**Register**) and 3D (**3D Preview**):
    1. Under the 2D option, which is the default option named **Register**, you can switch between four different views of the organ (Left, Right, Anterior, Posterior) and use your mouse to drag and drop the virtual square to the correct location.
    2. Under the **3D Preview** option, you can use your mouse to rotate the organ in three dimensions and use keyboard shortcuts to move the block ("W" and "S" for up-down, "D" and "A" for right-left, and "Q" and "E" for anterior-posterior).<br/>Once you are finished, click "Review and Register" and then "Register". This will close the popup and display the ID of your registry.
7. After choosing the appropriate values for other fields, click the _Save_ button. If there weren’t any errors, you will be redirected to the record page of the HRA 3D Coordinate you created.
8. Find the Specimen form tab that you were working on. Upon focusing on the page, the displayed option on the popup should update so you can see the newly created record.
9. Click the "Select" button (the blue button with the checkmark icon) on the row corresponding to the newly created HRA 3D Coordinate. The popup should close, and you should see the name of your registry on the HRA 3D Coordinate field.

You can now click on the Save button to save your changes. If there weren’t any errors, you will be redirected to the record page of the Specimen.

### 5.1 Editing an existing HRA 3D coordinate

1. Go to the Specimen page and make sure you are logged in.
2. From the "Refine search" sidebar, find the "HRA 3D Coordinate" filter and open it (it’s the second to last option).
3. Choose the "All records with value" option. The results table will now only display Specimen records that include HRA 3D Coordinate data.
4. You can choose a specific coordinate you want to edit instead of "All records with value".
5. Open any Specimen records by clicking on the “View” icon (document with magnifying glass icon).
6. In the opened Specimen record page, you should see the "HRA 3D Coordinate" field. Click on the field value, which is a link to the HRA 3D Coordinate record.
7. In the opened HRA 3D Coordinate record page, use the Edit button to navigate to the edit mode.

## 6. Adding an Antibody Record

If the slide was stained with an antibody, it's essential to record this data.

Go to the *Specimen Antibody* table and click `Add record` to add an antibody.

The important thing to fill out here is the *Antibody RID* to indicate the company. Click the field to see a list of existing companies in the catalog.

If you do not see the antibody company listed, click the **Create New** button to add it.

## 7. Associating Probes to Genes

For associating genes with specimens, populate the Specimen Probe Association table.

*Specimen Probe Association* is where you will associate the probe(s) with the data. The *Probe* table will display details of the probe(s) you chose - you do not manually add anything to this table.

Go to the *Specimen Probe Association* section and click the `Add record` link.

## 8. Documenting Gene Expression Scores

For In Situ Hybridization (ISH) data, make sure to add scored expression regions.

Go to the *Specimen Expression* table and click `Add record`.

There are various descriptive fields you may fill out, but at the very least, you’ll need to indicate the anatomical region and its expression score (the strength of expression in that region).

[![Screenshot of the fields for "Expression Region" and "Strength"](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-expression-scored-sm.png)](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/specimen-expression-scored.png)

Click the `Expression Region` field to choose the anatomical region.

Click the `Strength` field to choose from *uncertain*, *present*, and *not detected*.

## 9. Documenting Stages for Human Organoids

Documenting the organoid development stages ensures data uniformity and comprehension.

Kidney organoids are derived from pluripotent stems cells (ESC or iPSC) using a variety of possible protocols. To help standardize assignment of stages of organoid development, we will adopt the convention found in the published literature. This defines the onset of induction as Day 0.

- Day 0 = Induction of iPSCs or ESCs to begin differentiation (i.e. CHIR99021 added)

Each protocol may vary in the rate of formation subsequent to induction, thus the protocol used for a given experiment must be clearly documented with an entered specimen. This can be a reference to a protocol in the GUDMAP database, or the published paper that details the approach (include PMCID/PMID number).

**REFERENCES:**

>Takasato M, Er PX, Chiu HS, Maier B, Baillie GJ, Ferguson C, Parton RG, Wolvetang EJ, Roost MS, Chuva de Sousa Lopes SM, Little MH, 2015. Kidney organoids from human iPS cells contain multiple lineages and model human nephrogenesis. Nature 526, 564–568. PMID: 26444236

>Morizane R, Lam AQ, Freedman BS, Kishi S, Valerius MT, Bonventre JV, 2015. Nephron organoids derived from human pluripotent stem cells model kidney development and injury. Nat Biotechnol 33, 1193–1200. PMCID: PMC4747858

## 10. Finalizing Your Submission

Upon finalizing your records and internal reviews, submit them to the Hub by editing the Specimen record and change the *Curation Status* field to *Submitted*.

The biocurator will review your submission and may have more questions for improving the quality of your submission.

Once the biocurator and submitter are satisfied that the data is complete, the biocurator will change the *Curation Status* field to *Release*, at which time it becomes publicly accessible.
