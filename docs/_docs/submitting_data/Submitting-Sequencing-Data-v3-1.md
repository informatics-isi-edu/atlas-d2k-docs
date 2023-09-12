---
title: Submitting Sequencing/Omics Data
permalink: /docs/submitting-sequencing-data-v3-1/
---

**Table of Contents**
- [Introduction](#introduction)
- [1. Join the Correct Group](#1-join-the-correct-group)
- [2. Organize Your Data](#2-organize-your-data)
- [3. Add Specimen Records](#3-add-specimen-records)
- [4. Create Metadata Records](#4-create-metadata-records)
    - [4.1. Create Study Records](#41-create-study-records)
    - [4.2. Create Experiment Records](#42-create-experiment-records)
    - [4.3. Create Replicate Records](#43-create-replicate-records)
    - [4.4. Record and Curation Status Notes](#44-notes-about-record-status-and-curation-status)
- [5. Upload Files](#5-upload-sequencing-and-analysis-files)
    - [5.1. Review Supported File Extensions](#51-review-supported-file-extensions)
    - [5.2. Browser Upload Method](#52-upload-files-through-the-browser)
    - [5.3. Bulk Upload with Client Tools](#53-bulk-upload-through-our-client-tools)
- [6. Review and Submit](#6-review-internally-and-then-submit-to-the-hub)
    - [6.1. Data Submission Dashboard](#61-data-submission-dashboard)

## Introduction

This guide offers a clear pathway for submitting sequencing data to the ATLAS-D2K Data Explorer. For any questions, please contact [help@atlas-d2k.org](mailto:help@atlas-d2k.org). Always ensure you fill out all relevant fields to make your data discoverable and reproducible.

These are some other training materials and other documentation you may find useful:

* [Tutorial slides containing screenshots (Sequencing Model V3---latest)](https://docs.google.com/presentation/d/1dHg9LmThF7vXFYcUDmZ1s0IgmRhIT8qHAGnxkue1TCE/edit#slide=id.g3cef0a6f7b_0_412)
* [Advanced Editing Features](/docs/advanced-editing-features)
* [Tips for Submitting Large or Complex Data](Tips-for-Submitting-Large-or-Complex-Data)

## 1. Join the Correct Group

- Follow [these instructions](accessing-gudmap-and-rbk-resources/).
- If unsure about the group to join, contact [help@atlas-d2k.org](help@atlas-d2k.org).
- Remember to log in before submitting data.

## 2. Organize Your Data

Our system structures **metadata records** for efficient data discovery. They are organized as:
- **Study**: The top layer, including overarching objectives and designs. It may contain one or several Experiments.
    - **Experiment**: Comprises one or multiple Replicates with consistent methods. Linked records could include antibodies, custom metadata, and settings.
        - **Replicate**: Provides bio-sample details and both biological and technical replicate numbers. Replicates include:
          * All of the replicate-specific experimental assays, such as sequencing and analysis files.
          * A link to a **Specimen** record.  
          * For single cell RNA-Seq, you may also add a **Single Cell Metrics** record summarizing the statistics of a replicate.

### 2.1 Metadata Model for Sequencing Data

[![Chart of data model](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/ATLAS_Data_Model_Specimen.jpg)](https://raw.githubusercontent.com/informatics-isi-edu/gudmap-rbk/master/wiki_images/submitting-data/specimen/ATLAS_Data_Model_Specimen.jpg)

## 3. Add Specimen Records

For each tissue slide used, connect it to a **Specimen** record. Create these now and keep RID numbers handy for linking later. Comprehensive [specimen submission guidelines are available here](specimen-v2/).

## 4. Create Metadata Records

### 4.1. Create Study Records

- Use this link to log in and directly create a **Study** record: [https://www.atlas-d2k.org/chaise/recordedit/#2/RNASeq:Study](https://www.atlas-d2k.org/chaise/recordedit/#2/RNASeq:Study)
    - You can also go to any Study page and click `Create` in the record header (you must be logged in to see the `Create` button).
- Complete as many fields as are appropriate for your data and save.
- On the new Study record, scroll to the *Study Analysis File* section and click `Add` to add analysis files associated with your study.

### 4.2. Create Experiment Records

- On the Study record, navigate to the **Experiments** section and click `Add Record`.
- Fill in the fields describing your experiment and save.
- On the newly created Experiment, scroll down and link additional records such as **Experiment Antibodies**, to link to the antibodies used for cell isolation in the experiment, and  **Experiment Settings**, to enter the details related to processing the data.

### 4.3. Create Replicate Records

- From the Experiment record, scroll down to the **Replicate** section and click `Add record`.
- Link to one of the **Specimen** records you created earlier.
- Add the Biological and Technical Replicate Numbers:
    - The first replicate of an experiment will use the number `1` for both Biological and Technical Replicate numbers.
- Fill in all other fields relevant to your data.
- After completion, save the record.
- On the newly created Replicate record, link additional records:
    * **Files**: If you are only adding a few data files, scroll down to the **Files** table and click `Add`. To upload multiple files at the same time, you can click the plus sign (+) to add more forms. If you are uploading many or very large files, we recommend using the bulk upload method [described below](#53-bulk-upload-through-our-client-tools).
    * **Single Cell Metrics**: For single cell RNASeq data, scroll down to the **Single Cell Metrics** table and click `Add record` to include this information.

### 4.4. Record and Curation Status Notes

Remember:
- Incomplete records will indicate missing required information. The *Record Status* field will list which information is missing.
- Default status is "In preparation" and won’t be public till marked "Release".
- Once ready, switch status to "Submitted" for review. Upon approval, the status will change to "Release", making the data public.
- All records (e.g. Replicates, Specimen, Files) associated with an Experiment will have the same `Curation Status` as their Experiment. Once the Experiment is released, all those related records will also be released.
- Data submitters can control the Curation Status of a Study and Experiments within a Study; a Study that is released can have both Experiments that are released and ones that are not.  

## 5. Upload Files

The `.fastq` and `.bam` files are mandatory. However, data submitters are encouraged to also upload corresponding analysis files if they are available.

### 5.1. Review Supported File Extensions

Check the provided table for approved extensions and descriptions.

| Extension | File Type | Description (will appear in file caption) | mandatory |
|---|---|---|---|
| R1.fastq.gz | FastQ | F reads | mandatory |
| R2.fastq.gz | FastQ | R reads | mandatory for Paired-End |
| bam | bam | alignment | mandatory |
| bed | bed | positive regions | optional |
| bw | bigWig | visualization track | optional |
| rpkm.txt | txt | expression value | optional |
| tpm.txt | txt | expression value | optional |

### 5.2. Browser Upload Method

This method is suitable for fewer replicates and smaller files. For a quick guide:
- **Study** record: Add analysis files using the **Study Analysis File** section.
- **Replicate** record: Add sequencing and analysis files via the **File** section.

### 5.3. Bulk Upload with Client Tools

Suitable for many replicates or larger files. Follow [this tutorial](bulk-upload-tool/) to install and use.

## 6. Review and Submit

### 6.1. Data Submission Dashboard

The dashboard gives an overview of your submitted records. Ensure everything’s complete and accurate.

Before public release, the curation team reviews submissions. Once reviewed, the status becomes "Release" and data’s accessible.

---

For any queries, contact [help@atlas-d2k.org](mailto:help@atlas-d2k.org). Our team's always ready to support your data submission needs.
