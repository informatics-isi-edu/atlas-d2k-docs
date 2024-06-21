---
title: Submitting Specimen Data
permalink: /docs/specimen/
---

This guide will walk you through the steps to submit **biospecimen** and **imaging** data to the ATLAS-D2K Data Explorer. If you have any queries, please reach out to [help@atlas-d2k.org](mailto:help@atlas-d2k.org).

## Table of Contents

- [Metadata Model for Specimen Records](#metadata-model-for-specimen-records)
- [1. Joining the Globus Group](#1-joining-the-globus-group)
- [2. What is a Specimen Record?](#2-what-is-a-specimen-record)
    - [2.1 Overview for completing a Specimen record](#21-overview-for-completing-a-specimen-record)
    - [2.2 Organizing a Hierarchy of Specimen records](#22-organizing-a-hierarchy-of-specimen-records)
- [3. Submit Metadata Fields](#3-submit-metadata-fields)
    - [3.1. Fields for Specimen Records](#31-fields-for-specimen-records)
- [4. Link to Anatomy or Cell Type Terms](#4-link-to-anatomy-or-cell-type-terms)
    - [4.1. To Add the Same Anatomical Source to Several Specimen Records](#41-to-add-the-same-anatomical-source-to-several-specimen-records)
- [5. Link to a Publication](#5-link-to-a-publication)
    - [5.1 Fields for Publication Records:](#51-fields-for-publication-records:)
- [6. Upload Image Files](#6-upload-image-files)
    - [6.1. Fields for Image Records](#61-fields-for-image-records)
    - [6.2. Uploading Several Images](#62-uploading-several-images)
        - [6.2.1. Clone Records](#621-clone-records)
        - [6.2.2. Use DERIVA Client Tools](#622-use-deriva-client-tools)
    - [6.3 Add Image Channels](#63-add-image-channels)
        - [6.3.1 Fields for Image Channels](#631-fields-for-image-channels)
- [7. Upload Video Files](#7-upload-video-files)
    - [7.1. Field Descriptions for Video records](#71-field-descriptions-for-video-records)
- [8. Adding a new Human Reference Atlas (HRA) 3D coordinate (Human Adult Data Only)](#8-adding-a-new-human-reference-atlas-hra-3d-coordinate-human-adult-data-only)
- [9. Add Antibodies, Probes, Gene Expression Scores](#9-add-antibodies,-probes,-gene-expression-scores)
    - [9.1 Fields for *Specimen Antibody* records](#91-fields-for-specimen-antibody-records)
    - [9.2 Fields for *Specimen Probe Association* records](#92-fields-for-specimen-probe-association-records)
    - [9.3 Fields for *Specimen Expression* records](#93-fields-for-specimen-expression-records)
- [10. Other Information](#10-other-information)
- [11. Documenting Stages for Human Organoids](#11-documenting-stages-for-human-organoids)
- [12. Finalizing Your Submission](#12-finalizing-your-submission)


Follow the steps outlined to enhance the discoverability of your specimen and data. The more details you provide, the easier it is for users to discover your data.

## Metadata Model for Specimen Records

![Chart of Data Model for Specimen records]({{ "/assets/wiki_images/submitting-data/ATLAS_Data_Model_Specimen.jpg" | relative_url }})

<!-- TBD: Add caption that describes this chart and what the colors mean -->

## 1. Joining the Globus Group

To get editing access, join the relevant Globus group. Email [help@atlas-d2k.org](mailto:help@atlas-d2k.org) for assistance. For detailed information, see [Accessing ATLAS-D2K Resources](../accessing-atlas-resources/).

## 2. What is a Specimen Record?

A *Specimen* record describes the tissue from an organism (e.g., human, mice, organoid) used in your experiments. In ATLAS-D2K, these records host your imaging data and are linked to related [sequencing studies](../sequencing/).

Specimen records also house information such as antibodies that were used, expression scores and probes (among others).

### 2.1 Overview for completing a Specimen record

* [**Submit metadata**](#3-submit-metadata-fields). When you first create a Specimen record, you will fill out a form to submit metadata about the bio-tissue used in your experiment(s).

* [**Link to ontologies**](#4-link-to-anatomy-or-cell-type-terms). From the newly created Specimen record, you will link to an anatomy ontology term via the *Anatomical Source* field. Depending on the data, you may also link to a cell type ontology via the *Specimen Cell Type* field.

* [**Link to your publication**](#5-link-to-a-publication).

* [**Add image files.**](#6-upload-image-files) This is when you upload your 2D and/or 3D image files ([we also accept videos](#7-upload-video-files)).

* [**Add image channels**](#6.3-add-image-channels). If your images have multiple channels, you can describe them with Image Channels.

* [**Add/Link to Antibodies, Probes, Gene Expression Scores**](#9-add-antibodies,-probes,-gene-expression-scores). Depending on your experiments, you may also provide further information in these sections.

### 2.2 Organizing Specimen records (Parent/Child)

Many times, you will need to represent your Specimen records as a hierarchy, using Parent-Child relationships (sometimes Grandparent-Parent-Grandchild relationship). You may work with the Hub ([help@atlas-d2k.org](mailto:help@atlas-d2k.org)) directly to determine if you need such a hierarchy and how best to organize it.

The purpose of Specimen records and using a hierarchy is to make sure that in downstream analysis, it is always clear exactly which tissue (Specimen) was used to generate data.

An example of such a hierarchy is if an original tissue sample (Specimen A) is dissected into different samples for an experiment. Let’s say there are two of these samples, one for Histology imaging (Specimen B) and one for a Sequencing assay (Specimen C). In this case, you would first create a Specimen record for the original tissue (Specimen A) and this would be considered the Parent Specimen. Then Samples B and C would be Child Specimen records. These relationships are determined by the "Parent Specimen" field in the Specimen metadata (see section 3.1 below).

[TODO: ADD GRAPHIC HERE]

## 3. Submit Metadata Fields

* [Use this link to log in and create a Specimen](https://www.atlas-d2k.org/chaise/recordedit/#2/Gene_Expression:Specimen). Alternatively, from atlas-d2k.org,:
    - In the top-level menu, click *Internal*, then *Specimen*.
    - From a Specimen page, you can also click the `Create` button (you must be logged in to see this button).

* At a minimum, fill out the essential fields marked with a red asterisk (*). However, filling out more fields enhances data discoverability.

* Upon completion, click `Save`.

![Screenshot of the Create Specimen form]({{ "/assets/wiki_images/submitting-data/create-specimen-form.png" | relative_url }})

### 3.1. Fields for Specimen Records

<table>
  <tr>
    <th>Field</th>
    <th>Description</th>
    <th>Required/Optional</th>
  </tr>
  <tr>
    <td>Internal ID</td>
    <td>An important field for your own lab’s tracking purposes. This can be very useful to help you search for your Specimen records later and is critical if using the DERIVA client tools to bulk upload.</td>
    <td>Optional (but highly recommended)</td>
  </tr>
  <tr>
    <td class="required">Species</td>
    <td>e.g., Homo sapiens, Mus musculus.</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td>Stage</td>
    <td>The Theiler or Carnegie stage. If you cannot provide the stage, there is also the Chronological Age field where you can type in the age using free text.</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Chronological Age</td>
    <td>Free text field where you can manually enter the age of the specimen.</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td class="required">Assay type</td>
    <td>The imaging related types are IHC, ISH, and Histology.</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td class="required">Preparation, Fixation and Embedding</td>
    <td>These fields describe how the sample was prepared.</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td>Background Strain, Wild Type, Phenotype, Sex, Passage, Cell Line</td>
    <td>If available, provide further information about the specimen.</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Upload Notes, Probe Usage Notes, Experiment Notes and Results</td>
    <td>These fields are open text, Markdown-formatted text boxes and provide an opportunity to provide more context about the data.</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Acknowledgements</td>
    <td>Use this file to record people involved in processing this specimen for the experiment.</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Parent Specimen </td>
    <td>If you have subdivided a biological sample (e.g., you created sections from a sample), you can create a Specimen record for the original sample. Then for each section (child), designate the original sample as the "parent". You can continue doing this to show different levels of grandparent/parent/child relationships. </td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Representative Image</td>
    <td>This is an optional thumbnail of the image. If you do not add one, the system will automatically select the thumbnail from the first image record. Read this doc for our thumbnail guidelines.  </td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>HRA 3D Coordinate</td>
    <td>If the specimen is human, please register with the Human Reference Atlas Portal. Instructions are available in Section. 5 below. [ADD LINK]</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td class="required">Curation Status</td>
    <td>The default value is In Preparation which means this record is in draft mode and will only be viewable by other Consortium members who are logged in. For more information, see Curation Workflow.</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td class="required">Principal Investigator</td>
    <td>Choose the appropriate Principal Investigator. If your PI is not on the list, click the plus sign just to the top right of the list to create a new record for them.</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td class="required">Consortium</td>
    <td>Select GUDMAP or RBK.</td>
    <td class="required">Required</td>
  </tr>
</table>

Once you have saved the form, you will see a new Specimen record much like the following example:

![Screenshot of a Specimen record]({{ "/assets/wiki_images/submitting-data/specimen-record-page.png" | relative_url }})

## 4. Link to Anatomy or Cell Type Terms

From the Specimen record, link to at least one *Anatomical Source* from our list of ontology terms (from GUDMAP EMAPA or UBERON). This is **_required_**.

In the **Sections** list (left sidebar), look for the **Anatomical Source** and click the link. The field will scroll to the top of the page.

To the right of the field, click the `Link record` button. Start typing a term and choose your term from the list of available ontological terms.

* To indicate stem cell lines, search for "iPSC" or "hiPSC".

* You may enter more than one anatomical source, for example, if you entered iPSC or hiPSC, add another anatomical source and search for "podocyte", “kidney organoid”, etc.

![Anatomical Source field is highlighted in this screenshot]({{ "/assets/wiki_images/submitting-data/specimen-antomical-source.png" | relative_url }})

* To enter the cell line, click `Edit` for the Specimen record, scroll down to the **Cell Line** field and click the dropdown field to show available lines. Search for the cell line. If it is not available, you can click `Create new`, fill in the form and click `Save` to add it to the list.

If your data is at the cell level, link at least one *Specimen Cell Type* from the Cell Ontology. Note that this is a newer field. If you do not see the cell type terms you need, please contact **help@atlas-d2k.org**.

### 4.1. To Add the Same Anatomical Source to Several Specimen Records

This shortcut is handy if many Specimen records require the same Anatomical Source.

* Navigate to [Anatomy Facet Search](https://www.atlas-d2k.org/chaise/recordset/#2/Vocabulary:Anatomy/).

* Find the required anatomical term and click the `View Details` icon to open the page.

* Scroll down to the *Specimen* section and click `Link records` to link multiple Specimen records.

## 5. Link to a Publication

From the Specimen record, link to the related publication. In the **Sections** list (left sidebar), look for **Publication** and click the link. To the right of the field, click the `Link records` button.

![Anatomical Source field is highlighted in this screenshot]({{ "/assets/wiki_images/submitting-data/specimen-publication-field.png" | relative_url }})

If you know your publication has already been entered, search for the title and then click to link to the publication.

Otherwise, click the `Create new` button and fill out the fields with information about the publication. Click `Save` when you are finished.

### 5.1 Fields for Publication Records:

<table>
  <tr>
    <th>Field</th>
    <th>Description</th>
    <th>Required/Optional</th>
  </tr>
  <tr>
    <td class="required">Title</td>
    <td>Title of the publication</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td>Authors list</td>
    <td>List of authors, as they appear in the publication.</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Abstract</td>
    <td>Abstract of the publication</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td class="required">Publication venue</td>
    <td>Name of the journal or publication venue. If this is not available, you may click `Create new` to add an entry for the venue.</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td>Month</td>
    <td>Publication month</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td class="required">Year</td>
    <td>Publication year.</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td>Volume</td>
    <td>Journal volume.</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Issue</td>
    <td>Journal issue.</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Pages</td>
    <td>The pages where the publication appears.</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>PubMed ID</td>
    <td>The PubMed ID of the publication.</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>DOI</td>
    <td>The DOI reference.</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>URI</td>
    <td>Link from which the publication may be downloaded.</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Publisher Item Identifier</td>
    <td>A unique identifier, used by scientific journal publishers, to identify documents.</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>File URL</td>
    <td>Use this field to upload a PDF of the publication.</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td class="required">Curation Status</td>
    <td>Keep the default value of Submitted.</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td class="required">Principal Investigator</td>
    <td>The lead principal investigator of the publication.</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td class="required">Consortium</td>
    <td>Indicate GUDMAP or RBK.</td>
    <td class="required">Required</td>
  </tr>
</table>


## 6. Upload Image Files

You can upload 2D images and 3D images. Check the accepted [image file formats on this page](../standard-files-and-formats-for-submission/).

1. Go to the *Image* section.

2. Click the `Add records` button to the right of the section.

3. Fill out the fields and then click `Save`.

We highly recommend uploading a thumbnail file for the Image records. [Read this doc for our thumbnail guidelines.](../thumbnail-creation-guideline/).

**Note:** 3D image files were previously uploaded in a separate section. Those files are still avaiable in the section labeled *Image 3D (Legacy)*.

![Screenshot of Create Image form]({{ "/assets/wiki_images/submitting-data/image-record-form.png" | relative_url }})

### 6.1. Fields for Image Records

Although there are few required fields, the more fields you fill out, the more FAIR (findable, accessible, interoperable and reproducible) your data will be. Many of these fields will be especially helpful for the processing of lightsheet and other 3D imaging data in future pipelines.

<table>
  <tr>
    <th>Field</th>
    <th>Description</th>
    <th>Required/Optional</th>
  </tr>
  <tr>
    <td class="required">Image Dimension</td>
    <td>Choose 2D or 3D.</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td class="required">Media Type</td>
    <td>Select the format of the file. If a type is missing, please contact help@atlas-d2k.org.</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td class="required">Original File</td>
    <td>Use this field to select your file locally. If you have many files, they are especially large (> then 10GB) or are only accessible remotely, use see "Batch Upload Image Records" below)</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td>Pixels per Meter</td>
    <td>Number of pixels per meter associated with the image. This data represents pixel to physical scaling information.</td>
    <td>Only supply this if the uploaded image file does not contain this metadata.</td>
  </tr>
  <tr>
    <td>Thumbnail</td>
    <td></td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Microscope Instrument</td>
    <td>Name of the microscope used to capture the image. If your microscope is not listed, click the `Create new` button to add the name.</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Objective Numerical Aperture</td>
    <td>Lens numerical aperture (e.g., 0.156)</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Objective Magnification</td>
    <td>Lens magnification (e.g., 2x)</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Notes</td>
    <td>Use this field to add any clarification or description that may be useful to users.</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Acknowledgements</td>
    <td>Add the name and role of people who captured this data.</td>
    <td>Optional</td>
  </tr>
</table>


### 6.2. Uploading Several Images

#### 6.2.1. Clone Records

If you need to upload multiple image records simultaneously through the web interface, use the `Clone` button:

- Fill in the values of the field in the form that will be common across multiple records.
- Click the `Clone` button to create additional forms and edit individual ones as needed.

![Screenshot of a cloned image record form]({{ "/assets/wiki_images/submitting-data/image-record-cloned.png" | relative_url }})

#### 6.2.2. Use DERIVA Client Tools

If you have many files or your files are very large (over 5GB), then you may need to use our client tools for uploading files programmatically. See [Bulk Uploading Image Files](../bulk-uploading-image-files/) for more details.

### 6.3 Add Image Channels

For imaging data with multiple channels, you can designate their colors via the **Image Channel** field on the Image record. Historically, this information was entered in the free text **Notes** field and that is also an option.

To add Image Channels:

1. On the Image record you just created, scroll down to the **Image Channel** field and click the `Add records` button for each channel you want to add.

2. Fill out the fields and click `Save` when finished.

![Screenshot of a create image channel form]({{ "/assets/wiki_images/submitting-data/add-image-create-channel.png" | relative_url }})

#### 6.3.1 Fields for Image Channels

<table>
  <tr>
    <th>Field</th>
    <th>Description</th>
    <th>Required/Optional</th>
  </tr>
  <tr>
    <td class="required">Image</td>
    <td>This should already be set to the related Image record associated with this channel.</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td class="required">Channel Number</td>
    <td>This number indicates the order of this channel in the image file. Channel number starts with 0.</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td class="required">Name</td>
    <td>This is the channel name (name of the gene/protein displayed on the channel.)</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td>Pseudo Color</td>
    <td>The hexadecimal code for the channel color. You may either enter the code in the field or click the down arrow to use a color picker.</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Fluorophore</td>
    <td>Choose the fluorophore used in the channel. If the one you want is not listed, click the `Create new` button to add it.</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Representation</td>
    <td>Use this plain text field to indicate what this channel represents (e.g., rhodopsin, virus).</td>
    <td>Optional</td>
  </tr>

  <tr>
    <td>Notes</td>
    <td>This is a Markdown-formatted text field available for any additional information you want to provide.</td>
    <td>Optional</td>
  </tr>

</table>

## 7. Upload Video Files

You can also upload videos. Use these links to learn the accepted [video file formats](../standard-files-and-formats-for-submission/) and [video platforms](../available-video-platforms/).

1. Go to the *Video* section.

2. Click the `Add records` button to the right of the section.

3. Fill out the fields and then click `Save`.


### 7.1. Field Descriptions for Video records

<table>
  <tr>
    <th>Field</th>
    <th>Description</th>
    <th>Required/Optional</th>
  </tr>
  <tr>
    <td class="required">Title</td>
    <td>Provide the title describing the video.</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td class="required">File URL</td>
    <td>Use this field to select your file locally.</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td class="required">Media Type</td>
    <td>Select the format of the file. If a type is missing, please contact help@atlas-d2k.org.</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td class="required">Data Provider</td>
    <td>This is your lab's institution. If you need to add an institution, please contact help@atlas-d2k.org.</td>
    <td class="required">Required</td>
  </tr>
</table>

## 8. Adding a new Human Reference Atlas (HRA) 3D coordinate (Human Adult Data Only)

If your Specimen record is for *human adult* data, please follow the [instructions on this page](../register-human-atlas-reference/) to register it with HuBMAP's Human Atlas Reference using their Registration User Interface (RUI) tool (which has been integrated into the ATLAS-D2K system as of 2024).

## 9. Add Antibodies, Probes, Gene Expression Scores

There are many other types of information that you can connect with your Specimen record. In general, the process is the same:

1. Go to the desired section.

2. Click `Add record`.

3. Fill out the form fields and then click `Save` when you are finished.

The following tables guide you to details on the more common types of information to enhance your Specimen data. You can find field descriptions for each of these in the following sections:

<table>
  <tr>
    <th>If…</th>
    <th>Add records to these sections:</th>
  </tr>
  <tr>
    <td>the slide was stained with an antibody</td>
    <td>Specimen Antibody</td>
  </tr>
  <tr>
    <td>you are associating probes to genes</td>
    <td>Specimen Probe Association<br/><br/>

Note: The <em>Probe</em> section will display details of the probe(s) you chose - you do not manually add any records to this section.</td>
  </tr>
  <tr>
    <td>you are submitting In Situ Hybridization (ISH) data</td>
    <td>Specimen Expression</td>
  </tr>
</table>


### 9.1 Fields for *Specimen Antibody* records

<table>
  <tr>
    <th>Field</th>
    <th>Description</th>
    <th>Required/Optional</th>
  </tr>
  <tr>
    <td class="required">Antibody RID</td>
    <td>Choose from the list of existing companies in our Antibody Listings.  If you do not see the antibody company listed, click the Create New button to add it.</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td>Dilution</td>
    <td></td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Detection Method</td>
    <td></td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Lab ID</td>
    <td>Common name provided by the contributing lab (e.g., anti-Calb1)</td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Detection Notes</td>
    <td></td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Secondary Antibody</td>
    <td></td>
    <td>Optional</td>
  </tr>
</table>


### 9.2 Fields for *Specimen Probe Association* records

<table>
  <tr>
    <th>Field</th>
    <th>Description</th>
    <th>Required/Optional</th>
  </tr>
  <tr>
    <td class="required">Probe RID</td>
    <td>Choose from the list of existing probes.  If you do not see the probe listed, click the Create New button to add it.</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td>Strain</td>
    <td></td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Clone Name</td>
    <td></td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Tissue</td>
    <td></td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Product Label</td>
    <td></td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Final Label</td>
    <td></td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Probe Type</td>
    <td></td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Probe Origin Type</td>
    <td></td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Probe Stage Format</td>
    <td></td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Probe Stage</td>
    <td></td>
    <td>Optional</td>
  </tr>
  <tr>
    <td class="required">Curation Status</td>
    <td>The default value is In Preparation which means this record is in draft mode and will only be viewable by other Consortium members who are logged in. For more information, see <a href="../curation-workflow/">Curation Workflow</a>).</td>
    <td class="required">Required</td>
  </tr>
</table>


### 9.3 Fields for *Specimen Expression* records

For In Situ Hybridization (ISH) data, make sure to add scored expression regions in this section.

<table>
  <tr>
    <th>Field</th>
    <th>Description</th>
    <th>Required/Optional</th>
  </tr>
  <tr>
    <td class="required">Expression Region</td>
    <td>Indicate the anatomical region by searching through ontology terms.</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td class="required">Strength</td>
    <td>Select a value to indicate the strength of expression in that region. Choose from uncertain, present, and not detected.</td>
    <td class="required">Required</td>
  </tr>
  <tr>
    <td>Strength Modifier</td>
    <td></td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Pattern</td>
    <td></td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Pattern Location</td>
    <td></td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Density</td>
    <td></td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Density Change</td>
    <td></td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Density Magnitude</td>
    <td></td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Density Relative To</td>
    <td></td>
    <td>Optional</td>
  </tr>
  <tr>
    <td>Density Note</td>
    <td></td>
    <td>Optional</td>
  </tr>
</table>

## 10. Other Information

The following are additional types of information that may be added to a Specimen record:

<table>
  <tr>
    <th>Section</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>Derived Specimen</td>
    <td>If there is a Parent Specimen, it will be listed here (or is it the other way around, this is where Child Specimen would appear?)</td>
  </tr>
  <tr>
    <td>Specimen Allele</td>
    <td></td>
  </tr>
  <tr>
    <td>Probe</td>
    <td>Lists any probes that were linked under Specimen Probes.</td>
  </tr>
  <tr>
    <td>Anchor Gene Specimen</td>
    <td></td>
  </tr>
  <tr>
    <td>Marker Gene Specimen</td>
    <td></td>
  </tr>
  <tr>
    <td>Mouse Strain Characterized by this Specimen</td>
    <td></td>
  </tr>
  <tr>
    <td>Specimen Mouse Strain</td>
    <td>Lists any mouse strains that were characterized using the previous section (?)</td>
  </tr>
  <tr>
    <td>Study Replicate</td>
    <td>Links to any sequencing data related to this Specimen via the Replicate records in a Study.</td>
  </tr>
  <tr>
    <td>Legacy RNASeq Sample</td>
    <td></td>
  </tr>
  <tr>
    <td>Microarray Sample</td>
    <td></td>
  </tr>
  <tr>
    <td>Specimen Collection</td>
    <td>Links to any Data Collections that link to this Specimen.</td>
  </tr>
</table>


## 11. Documenting Stages for Human Organoids

Documenting the organoid development stages ensures data uniformity and comprehension.

Kidney organoids are derived from pluripotent stems cells (ESC or iPSC) using a variety of possible protocols. To help standardize assignment of stages of organoid development, we will adopt the convention found in the published literature. This defines the onset of induction as Day 0.

* Day 0 = Induction of iPSCs or ESCs to begin differentiation (i.e. CHIR99021 added)

Each protocol may vary in the rate of formation subsequent to induction, thus the protocol used for a given experiment must be clearly documented with an entered specimen. This can be a reference to a protocol in the GUDMAP database, or the published paper that details the approach (include PMCID/PMID number).

**REFERENCES:**

>Takasato M, Er PX, Chiu HS, Maier B, Baillie GJ, Ferguson C, Parton RG, Wolvetang EJ, Roost MS, Chuva de Sousa Lopes SM, Little MH, 2015. Kidney organoids from human iPS cells contain multiple lineages and model human nephrogenesis. Nature 526, 564–568. PMID: 26444236

>Morizane R, Lam AQ, Freedman BS, Kishi S, Valerius MT, Bonventre JV, 2015. Nephron organoids derived from human pluripotent stem cells model kidney development and injury. Nat Biotechnol 33, 1193–1200. PMCID: PMC4747858

## 12. Finalizing Your Submission

Once you are finished with your internal review, submit your records to the Hub by editing the Specimen record and change the **Curation Status** field to **Submitted**.

The Biocurator will review your submission and may have more questions for improving the quality of your submission.

Once the Biocurator and submitter are satisfied that the data is complete, the Biocurator will change the **Curation Status** field to **Release**, at which time it becomes publicly accessible.
