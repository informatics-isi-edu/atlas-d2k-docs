---
title: Submitting Histology Data
permalink: /docs/histological-data/
---

<!-- uncomment when generating PDF in Atom
# Submitting Histology Data
-->
<!-- comment out when generating PDF in Atom  
**[PDF version](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Submitting-Histology-Data.pdf)**
-->
This page provides instructions for adding histological (H&E) images to the ATLAS-D2K Data Explorer.

If you have any questions or feedback, please send them to your consortium's help email: [help@atlas-d2k.org](mailto:help@atlas-d2k.org).

We also have the following training materials available:
* [Webinar Slides](/asssets/slides/GUDMAP-RBK-12122017-data_submission_workshop-he.pptx?raw=true)
* [Webinar Replay (18:40)](https://youtu.be/fY9wQmn4KE0)
* Tutorial Videos (Coming Soon)

<a name="overview"/>

## Overview

Adding histological slides involve the following steps:

* Make sure you are in the correct Globus authentication group ([follow the instructions on this page](accessing-gudmap-and-rbk-resources/)), and that you are logged in.
* Create a new Histological Slide record.
* Fill out the form and upload your CZI file.
* Once the slide is submitted to the Hub (via the _Curation Status_ field), the system will process the image.
* The image is then displayed in the browser via a special viewer that displays channels, a scale bar, and allows you to zoom in and out and create annotations.


<div class="page-break"></div>
<a name="schema"/>

## Schema

![Histological Slide schema diagram]({{ "/assets/wiki_images/submitting-data/hist-schema.png" | relative_url }})

The schema for histological slides is very simple - the record for the slide and then the system-generated image.


<div class="page-break"></div>
<a name="globus"/>

## Join the correct group

[Follow the instructions on this page](accessing-gudmap-and-rbk-resources/). If you're not sure which group you need to join, please contact [help@atlas-d2k.org](help@atlas-d2k.org).

<a name="create slide"/>

## 1. Create Histological Slide record

* In the top navigation bar, click _Create > Histological Images_.

    ![Screenshot of Histological Slide record create form]({{ "/assets/wiki_images/submitting-data/create-he-slide.png" | relative_url }})


<div class="page-break"></div>


* The "Create Histological Slide Record" form appears:

    ![Screenshot of Histological Slide record create form]({{ "/assets/wiki_images/submitting-data/hist-create-form.png" | relative_url }})


<div class="page-break"></div>

* Select the values for each relevant field. The **required** fields are listed, but the more fields you fill out the easier the data is to find:
  * _Name_: Please use a short descriptive name to help users understand what the image represents.
  * _Download Link_: Upload the raw CZI file.
  * _Tissue_
  * _Age Stage_
  * _Specimen Fixation_
  * _Embedding Medium_
  * _Staining Protocol_
  * _Curation Status_: Choose either:
    * _In Preparation_: Use this status while still drafting the data.
    * _PI Review_: Use this status when your data is ready for internal review.
    * _Submitted_: Use this status when your data is ready for Hub review.
    * **Note:** Your data will **not** be viewable publicly until approved for _Release_ by the Hub. [For a complete description of the Curation Process, click here.](/docs/curation-workflow)
  * _Principal Investigator_
  * _Data Provider_
  * _Consortium_

* Scroll back up to the top of the page and click the _Submit_ button to save the record.


<div class="page-break"></div>

## 2. Reviewing and Submitting Histological slides

**Note: By the hard launch of the new GUDMAP site in April, there will be dashboards and email notifications to make this process more straightforward. In the meantime, here is how a project's PI or designated reviewer can find their project's data with a Curation Status of "PI Review"**

* Make sure you are logged in.

* From the navigation bar, click _Data > Gene Expression Data > Histological Images_.

* In the faceting sidebar on the left, scroll to **Curation Status** and choose _PI Review_. Note: Keep in mind that the data submitter may have forgotten to set the Curation Status field, in which case the status would still be _In Preparation_.

* In the faceting sidebar, scroll to **Principal Investigator** and choose your project's PI. Now you should see the data you need to review.

* When your record is approved internally, change _Curation Status_ to _Submitted_ to send it to the Hub (click here for the full [Curation Workflow](/docs/curation-workflow)).

<!--
* From the navigation bar, click _Data > Gene Expression Data > Histological Images_.

    ![Screenshot of using navbar to search histological slides]({{ "/assets/wiki_images/submitting-data/search-he-slide.png" | relative_url }})

* Use the filtering sidebar to narrow down the results by an attribute such as Principal Investigator.

    ![Screenshot of filtering for PIs]({{ "/assets/wiki_images/submitting-data/hist-filter-records-pi.png" | relative_url }})

    OR

    Type an identifying attribute into the search field above the search results.

    ![Screenshot of using search field to search for histological slides]({{ "/assets/wiki_images/submitting-data/hist-filter-records-search.png" | relative_url }})
-->

<div class="page-break"></div>

## 3. Processing the CZI file

Once you have finished any internal review designated by your lab and you set the _Curation Status_ to _Submitted_, the CZI file will be added to the system queue for processing.

The system runs a script every hour that looks in the queue and processes the CZI files there, which will take an additional 30 minutes per file. So it may take up to 1-2 hours for your CZI file to be processed and available in the viewer. The raw file is then immediately available.

Here is an example of a processed CZI file within the viewer:

![Screenshot of Histological image]({{ "/assets/wiki_images/submitting-data/hist-image-example.png" | relative_url }})


<!--
<a name="annotations"/>

## Adding Annotations

To add annotations to the processed CZI file:

* Go to the slide record and make sure you are logged in.

* Scroll down to the "Images" section and click the "Annotations" button above the image you want to annotate.

images

* Click the "Create Annotation" button and click and drag the part of the image you want to annotate.

images

A new small form appears: "New Rectangle Annotation".

images

* Add a description, choose the appropriate anatomical term from the dropdown list and click Submit.
-->

<div class="page-break"></div>

<a name="delete"/>

## 4. Deleting Histological Slides

To delete the Histological slide record, you must first delete the system-generated image.

* Go to the record you want to delete (see previous section).

* Scroll down to the "Images" section and click "Table Display" (a link to the right side of the section).

    ![Screenshot of the "Table Display" link next to the Histological Slides Image]({{ "/assets/wiki_images/submitting-data/hist-delete-table.png" | relative_url }})

* For each image, click the trashcan (Delete) icon in the "Actions" column. A confirmation window will open - click "Confirm".

    ![Screenshot of the Trashcan icon]({{ "/assets/wiki_images/submitting-data/hist-delete-unlink.png" | relative_url }})

* Once all the images in this table are deleted, scroll back up to the top of the record and click "Delete" in the record header.

    ![Screenshot of the "Delete" link in the record header]({{ "/assets/wiki_images/submitting-data/chaise-delete-option.png" | relative_url }})
