---
title: Tips for Submitting Large or Complex Data
permalink: /docs/tips-for-submitting-large-or-complex-data/
---

<!-- uncomment when generating PDF in Atom 
# Tips for Submitting Large or Complex Data
-->
<!-- comment out when generating PDF in Atom -->

**[PDF version](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Tips-for-Submitting-Large-or-Complex-Data.pdf)**

The following is a recommended workflow when you are submitting specimen or sequencing data with many files, large files (over 5GB or so) or you have a complex organization (ie, many experiments with many replicates each).

Read [Submitting Sequencing Data](/docs/submitting-sequencing-data-v3) and [Submitting Specimen Data](/docs/specimens) for full details about the process. The following is a more concise version with helpful shortcuts.

We also recommend reading [Advanced Editing Features](/docs/advanced-editing-features) for more features that make the data entry process much faster and more efficient.

**Features:**

- [1. Take advantage of Internal IDs](#1-take-advantage-of-internal-ids)
- [2. Create Specimen records](#2-create-specimen-records)
- [3. Create multiple Sequencing records at a time](#3-create-multiple-sequencing-records-at-a-time)
- [4. Uploading Multiple Files](#4-uploading-multiple-files)

## 1. Take advantage of Internal IDs

Consider a convention for the Internal ID you'll use for your Specimen, Study and Experiment records, especially if you will be using the bulk upload. This makes it easier to go back and find your entries and are also used for the directory names in bulk upload.

For example, if you use a similar prefix for Internal IDs of all your Specimen that is unique to your data submission, you can search just the prefix to pull up all the Specimen records you're currently working with.

## 2. Create Specimen records 

(The following focuses more on the use of Specimen records in sequencing data submissions, but you can use similar techniques for Specimen submissions.)

For each slide of tissue used in your sequencing experiments, you will need to create a corresponding Specimen record. Create your Specimen records now and note the RID numbers so you can link them to your Sequencing data later.

  - Use [multi-create](/docs/advanced-editing-features#1-multi-create) to create batches of specimen for each slide of tissue (up to 10 records at a time is recommended according to your network strength). Use your **Internal ID** to keep track of them. 
      - Go to a Specimen search page and click `Create`. 
      - Add any common values that you'll be using across all Specimen records.
      - Click the plus sign (+) to add more records. The values you entered in the first record will also be copied.
      - You may only want to add up to 10 at a time (depending on the strength and stability of your network).
  - Add **Anatomical Source** to each Specimen record. Here's the fast way to add the same Anatomical Source to multiple Specimen records:
      1. Go to _Search > Anatomy Terms > Faceted Search_ in the menu. 
      2. Search or filter to find the anatomical term and click its eye icon.
      3. Click `Specimens` in the right Content sidebar or scroll down to that section, then click `Add` to the right of the table.
      4. In this window, you can filter or search for your Specimens, check their boxes, click Submit and now they will be associated with this Anatomical Term. 

## 3. Create multiple Sequencing records at a time

  - Create a Study (this is the "container" record for a group of experiments).
  - On the Study record, go to the Experiment section and click `Add`. In the form, use multi-create (the plus sign) to create many experiments together. 
  - Create batches of replicates: 2 options
     - Go to each individual Experiment record, scroll to the Replicate section, then click `Add`. Multi-create all replicates per experiment at once. This option will automatically link the replicates to the experiment. 
     - From the navbar, click _Create -> Sequencing Data -> Replicate_. Multi-create replicates, but you will have to specify which Experiments they should be linked to yourself. In this case, you could fill in the experiment RID on the first replicate form (search using the RID or Internal ID), then click the plus sign to add as many replicates for that experiment as you need.

## 4. Uploading Multiple Files

At this point, you can go to the **Files** section of a Replicate, click `Add` and multi-create many files which you can upload at the same time (although there are limits depending on the strength and stability of your network). 

But if you have many files or some large files to upload, it will be much more efficient to use our client tools on the command-line.

You can find the documentation on [Bulk Uploading here](/docs/bulk-upload-with-deriva-client-tools). The major steps are:

- Follow the instruction on how to create a folder structure and name your files. 
- Then download the software and follow the instructions to submit an upload job for all of the files. 

If you named your directories and files correctly, they will now be associated with the proper Replicate records.


