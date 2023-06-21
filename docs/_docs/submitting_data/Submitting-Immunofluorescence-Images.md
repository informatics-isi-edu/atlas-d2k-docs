---
title: Submitting Immunofluorescence Images
permalink: /docs/immunofluorescence-images/
---

<!-- uncomment when generating PDF in Atom 
# Submitting Immunofluorescence Images
-->
<!-- comment out when generating PDF in Atom -->
**[PDF version](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Submitting-Immunofluorescence-Images.pdf)**


This page provides instructions for adding immunofluorescence image data to the ATLAS-D2K Data Explorer.

If you have any questions or feedback, please send them to your consortium's help email: [help@gudmap.org](mailto:help@gudmap.org) or [help@rebuildingakidney.org](mailto:help@rebuildingakidney.org)

We also have the following training materials available:
* [Webinar Slides](/assets/slides/GUDMAP-RBK-12132017-data_submission_workshop-if.pptx?raw=true)
* [Webinar Replay (30:41)](https://youtu.be/UrG8vnBE1YQ)
* Tutorial Videos (Coming Soon)

<a name="overview"/>

## Overview

Adding immunofluorescence slides to the Data Browser involves the following steps:

* Make sure you are in the correct Globus authentication group, [kidney-writers](/docs/protocols#1-join-the-kidney-writers-group), and that you are logged in.
* Create a base "Slide Record" with basic metadata and uploaded image file. 
* Optionally, link other data to this record: genes, expression regions, antibodies and videos.

<div class="page-break"></div>

<a name="schema"/>

## Schema

The following represents how different tables in the Data Browser are related in order to form the Immunofluorescence data record.

![Screenshot of IF slide record form](/assets/wiki_images/submitting-data/if-schema.jpg)

<a name="globus"/>

## Are you in the `kidney-writers` group?

If you haven't already done so, go to this link to join the group: [https://app.globus.org/groups/af0b4010-5b75-11e6-9575-22000aef184d/about](https://app.globus.org/groups/af0b4010-5b75-11e6-9575-22000aef184d/about)

You can find more details about this process at [Accessing ATLAS-D2K Resources](/docs/accessing-gudmap-and-rbk-resources).


<div class="page-break"></div>

<a name="create-slide"/>

## 1. Create the IF slide record

* In the top navigation bar, click _Create > Immunofluorescence Images_.

    ![Screenshot of Histological Slide record create form](/assets/wiki_images/submitting-data/if-navigation.png)

<div class="page-break"></div>
  
*  The Create form appears.
  
    ![Screenshot of IF slide record form](/assets/wiki_images/submitting-data/if-slide-record-form.png)
  
  <div class="page-break"></div>
  
  * Select the values for each relevant field. The **required** fields are listed, but the more fields you fill out the easier the data is to find:
    * _Name_: Please use a short descriptive name to help users understand what the image represents.
    * _Download Link_: Upload the slide image.
    * _Slide Type_: Choose whether this slide is wholemount or a section.
    * _Curation Status_: Choose either
      * _In Preparation_: Use this status while still drafting the data.
      * _PI Review_: Use this status when your data is ready for internal review. 
      * _Submitted_: Use this status when your data is ready for Hub review. 
      * **Note:** Your data will **not** be viewable publicly until approved for _Release_ by the Hub. [For a complete description of the Curation Process, click here.](/docs/curation-workflow)
    * _Principal Investigator_: Choose the name of your project's contact PI.
    * _Data Provider_: Choose the lab/institution associated with this data.
    * _Consortium_: Make sure you indicate whether this is from the ATLAS-D2K consortium.

* Scroll back up to the top of the page and click the _Submit Data_ button to save the record.

    ![Screenshot of IF slide record form](/assets/wiki_images/submitting-data/chaise-submit.png)


<div class="page-break"></div>
    
<a name="antibodies-genes"/>

## 3. Adding genes, expression regions and antibodies

Once you have the basic Slide record, scroll down further to view other types of data you may associate (link) with the slide: _Genes, Expression Regions and Antibodies_. For each of these sections, the procedure is basically the same: 

* Find the Slide record you want to link records to by clicking _Search > Gene Expression Data > Immunofluorescence Slides and Video_ in the navigation bar and searching for the record (per the previous section).
  
* Click the eye icon in the _Actions_ column to view the desired record.

  ![Clicking the eye icon to view](/assets/wiki_images/submitting-data/if-viewing.png)
  
* Make sure you are logged in.
* Scroll down to the desired section and click _Add_ on the right side of the page.

![Clicking the Add link of the gene section](/assets/wiki_images/submitting-data/if-add-link.png)

* Search for existing data and select it (you may select multiple values). Then click the _Submit_ button (see the following screenshot).

![Search and select window](/assets/wiki_images/submitting-data/if-search-select.png)

<div class="page-break"></div>

<a name="video"/>

## 4. Adding video

* Scroll down to the **Slide Videos** section and click the _Add_ link on the right side of the page.

![Create Slide Video Record form window](/assets/wiki_images/submitting-data/if-add-link-video.png)

* Fill out the **Create Slide Video Record** form. 

![Create Slide Video Record form window](/assets/wiki_images/submitting-data/if-create-slide-video-record.png)

* Upload your video file by clicking on the _Select File_ button in the _Download Link_ field. **Note: At this time, please submit mp4 file format. This allows users to view the movie in the browser window.** For best results, use 16:9 aspect ratio and high resolution (ideally 1080p).

![Download link](/assets/wiki_images/submitting-data/if-create-slide-video-record-download.png)


* Click the _Submit Data_ button.


<div class="page-break"></div>
<a name="reviewing-submitting"/>

## 5. Reviewing and Submitting Immunofluorescence Data

**Note: By the hard launch of the new GUDMAP site in April, there will be dashboards and email notifications to make this process more straightforward. In the meantime, here is how a project's PI or designated reviewer can find their project's data with a Curation Status of "PI Review"**

* Make sure you are logged in.

* From the navigation bar, click _Search > Gene Expression Data > Immunofluorescence Images and Video_.

* In the faceting sidebar on the left, scroll to **Curation Status** and choose _PI Review_. Note: Keep in mind that the data submitter may have forgotten to set the Curation Status field, in which case the status would still be _In Preparation_.

* In the faceting sidebar, scroll to **Principal Investigator** and choose your project's PI. Now you should see the data you need to review.

* When your record is approved internally, change _Curation Status_ to _Submitted_ to send it to the Hub (click here for the full [Curation Workflow](/docs/curation-workflow)).

<div class="page-break"></div>

<a name="delete"/>

## 6. Deleting Immunofluorescence Data

Before you can delete the base record, you need to unlink (delete) any records associated with it.

To delete an IF Slide record:

* Scroll down the record to the sections for Genes, Expression Regions, Antibodies and Videos.
* In each of these sections, unlink the entries by clicking the 'x' icon in the _Actions_ columns.

![Unlink Gene](/assets/wiki_images/submitting-data/if-unlink-gene.png)

* Once all of the related records have been unlinked (deleted), then scroll up to the top of the record and click _Delete_.

![Delete button](/assets/wiki_images/submitting-data/chaise-delete-option.png)
