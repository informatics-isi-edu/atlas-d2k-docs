---
title: Submitting Antibodies
permalink: /docs/antibodies/
---

<!-- uncomment when generating PDF in Atom 
# Submitting Antibody Data
-->
<!-- comment out when generating PDF in Atom -->
**[PDF version](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Submitting-Antibodies.pdf)**

This page provides instructions for adding antibody validation data to the GUDMAP/RBK Data Explorer.

If you have any questions or feedback, please send them to your consortium's help email: [help@gudmap.org](mailto:help@gudmap.org) or [help@rebuildingakidney.org](mailto:help@rebuildingakidney.org)

We also have the following training materials available:
* [Webinar Slides](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/slides/GUDMAP-RBK-12112017-data_submission_workshop-antibodies.pptx?raw=true)
* [Webinar Replay 12/11/2017 (37:08)](https://youtu.be/3bQMSogtVY4)

<a name="overview"/>

## Overview

Adding antibody validation data involves the following steps:

* Make sure you are in the correct Globus authentication group, [kidney-writers](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Submitting-Protocols#1-join-the-kidney-writers-group), and that you are logged in.
* Search that antibody data already exists for your test.
* If it doesn't, then create an antibody record.
* Create an antibody test record.
* Add distribution terms to your antibody test record.
* Add any images or other media.
* Add a test summary sheet.
* You may also 'bulk add' several test records if they are similar (ie, only the media type and outcome are different).

<a name="schema"/>

<div class="page-break"></div>

## Schema

![Antibody schema diagram](wiki_images/submitting-data/antibody_schema.jpg)

The Antibody schema contains two main tables:
* Antibodies: General product information about each antibody, similar to what might be found on the manufacturer's website.
* Antibody Tests: Information about researchers' experience using each antibody.

Other related tables include:
* Antibody Media Files: Images and other media files related to antibody tests (slide images, summary PDFs, etc.)
* Test Methods: Descriptions of the methods used in antibody tests.
* Various vocabulary tables.

<a name="globus"/>

<div class="page-break"></div>

## 0. Are you in the `kidney-writers` group? (Required)

If you haven't already done so, go to this link to join the Globus group: [https://app.globus.org/groups/af0b4010-5b75-11e6-9575-22000aef184d/about](https://app.globus.org/groups/af0b4010-5b75-11e6-9575-22000aef184d/about)

You can find more details about this process at [Accessing GUDMAP and RBK Resources](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Accessing-GUDMAP-and-RBK-Resources).

**NOTE: We only use Globus for authentication, not for file or data management.**

<a name="search-antibody"/>

## 1. Search for the antibody you're working on

* Go to https://www.gudmap.org/chaise/recordset/#2/Antibody:Antibodies@sort(Protein_Target,RID) and log in.

* This will take you to the antibody search page, which you can use to find out if the antibody you're working on is already listed in our database. Start typing the name of the antibody in the search field or use the filtering sidebar on the left to narrow down the results.

![Screenshot of antibodies search page](wiki_images/submitting-data/antibody-search-page.png)


* If your antibody is there, you can go ahead and create the antibody test record (See next section). If not, move on to the next step below.



<div class="page-break"></div>
<a name="create-antibody"/>

## 2. If you cannot find the antibody, create a new antibody record

If you did find the antibody, move on to the next step.

* From the navigation bar, click _Create > Antibody > Antibodies_.
  
  The `Create Antibodies Record` form opens in a new browser tab.
  
  ![Screenshot of the Create Antibodies form](wiki_images/submitting-data/create-antibody.png)
  
* Select the values for each relevant field. The **required** fields are:
  * _Company ID_ 
  * _Catalog Number_
  * _Host Species_
  * _Protein Target_: Note that this list comes from the NCBI Gene List and should include all proteins. Also, you will soon be able to search on synonyms. 
  * _Curation Status_: Choose either
    * _In Preparation_ (still drafting), 
    * _PI Review_ (ready for internal approval), or 
    * _Submitted_ (ready for Hub review). Your data will **not** be viewable publicly until approved for _Release_ by the Hub. [For a complete description of the Curation Process, click here.](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Curation-Workflow)
  * _Consortium_: Make sure you indicate whether this is from the RBK or GUDMAP Consortium.
  
* When finished, click `Submit Data` to save your new antibody record. You can now close this tab.

### What if my antibody is not from a vendor?

If your antibody is not from a vendor (ie, it's a donated reagent), then you may choose a name for the _Company ID_ ("Donated reagent from X Lab") and use the RRID for the _Catalog Number_ or some other unique identifier.

<div class="page-break"></div>

<a name="create-antibody-test"/>

## 3. Create your new antibody test record

* From the navigation bar, click _Create > Antibody > Antibody Test_. 

    The `Create Antibody Test Record` form appears in a new browser tab.

    ![Screenshot of the Create Antibody Test Record form](wiki_images/submitting-data/create-antibody-test.png)

* Select the values for each relevant field. The required fields are:
  * _Antibody Product ID_
  * _Protein Target_: Note that this list comes from the NCBI Gene List and should include all proteins. Also, you will soon be able to search on synonyms. 
  * _Curation Status_: Choose either
    * _In Preparation_ (still drafting), 
    * _PI Review_ (ready for internal approval), or 
    * _Submitted_ (ready for Hub review). Your data will **not** be viewable publicly until approved for _Release_ by the Hub. [For a complete description of the Curation Process, click here.](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Curation-Workflow)
  * _Principal Investigator_: Choose the name of your project's contact PI.
  * _Consortium_: Make sure you indicate whether this is from the RBK or GUDMAP consortium.
  
* Note: If you are creating multiple antibody test records, you may click the `+` button (under the `Submit Data` button) to copy over the record form. Each time you click `+` will display a copy of the most recent form that you can edit as needed.

![Screenshot of the multiple antibody test records](wiki_images/submitting-data/create-antibody-test-batch.png)
  
* When finished, click `Submit Data` to save your new antibody test record(s).

* If you are not finished with your submission, you may still save your work by clicking the `Submit Data` button. Then you may go back to the record, log in and click `Edit` to resume filling it out. 

![Screenshot of the Edit button](wiki_images/submitting-data/general-record-header-edit.png)


<div class="page-break"></div>

<a name="distribution"/>

## 4. Add distribution terms to your antibody test record

* Scroll to the bottom of the antibody test record until you see a section labelled `Distribution`. This is our term for cell types / anatomical regions relevant to this antibody test.

* Click `Add` in the `Distributions` section. 

![Screenshot pointing out the Add link in the Distribution section](wiki_images/submitting-data/antibody-test-example-distribution-add.png)

  This will bring up a `Create Antibody Test Distribution Record` window.
  
  <div class="page-break"></div>
  
* Start typing the anatomical term in the search term to narrow your results.

![Screenshot of searching for distribution terms](wiki_images/submitting-data/antibody-test-example-distribution-search.png)

* Click `Select a value`
* Click the checkmark to the left of your desired distribution value.
* Click `Submit Data` to add the distribution.
* Repeat for as many distributions as desired.

<div class="page-break"></div>

<a name="test-results"/>

## 5. Add test summary sheets and images

Near the bottom of the newly-created antibody test record, you'll see empty sections labelled `Test Summary Sheets` for PDF summaries of the test, and `Test Images` for slide images relevant to the test.

![Screenshot of Test Summary Sheets and Test Images sections](wiki_images/submitting-data/antibody-test-example-media-files-sections.png)

<div class="page-break"></div>

To add a test-related files:

* Click `Add` in the `Test Images` or `Test Summary Sheets` section. 

![Screenshot of Add links](wiki_images/submitting-data/antibody-test-example-files-add.png)

<div class="page-break"></div>

  This will bring up the `Choose Antibody Media Files` window.
  
![Screenshot of the Choose Antibody Media Files window](wiki_images/submitting-data/antibody-choose-media-files.png)

* If the desired file has already been uploaded, select it.

<div class="page-break"></div>

* If not, upload your file:

    * Click the `+` at the top right-hand side of the `Choose Antibody Media Files` window. 
    
    ![Screenshot of the add button in the Choose Antibody Media Files window](wiki_images/submitting-data/antibody-choose-media-files-add.png)
    
    <div class="page-break"></div>
    
    This will open a `Create Antibody Media Files Record` page in a separate browser tab.
    
    ![Screenshot of the Create Antibody Media Files window](wiki_images/submitting-data/antibody-create-media-files.png)
    
    * Click on `Select File` to select a file from your computer. Either an image file if you're adding a test image or a PDF for the test summary.
    
    ![Screenshot of the Select File button in the Create Antibody Media Files window](wiki_images/submitting-data/antibody-create-media-files-select.png)
    
* Please use the _Comment_ Field to paste in the summary of the test result doc from the PDF.    
* Fill in the rest of the fields on the form. Required fields are:
      * _Principal Investigator_: Choose the name of the contact PI for your project. If their name isn't available, please contact the Hub.
      * _Curation Status_: Choose either
        * _In Preparation_ (still drafting), 
        * _PI Review_ (ready for internal approval), or 
        * _Submitted_ (ready for Hub review). Your data will **not** be viewable publicly until approved for _Release_ by the Hub. [For a complete description of the Curation Process, click here.](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Curation-Workflow)
      * _Data Provider_: This is your lab's institution. If you need to add an institution, please contact the Hub.
      * _Consortium_: Make sure you indicate whether this is from the RBK or GUDMAP consortium.
      * _Description_: This is not required - however, this field is useful for test images if you want to describe what different colors represent, etc.

* Click `Submit Data` to complete the upload.

* Go back to the browser tab of your Antibody Test Record and select your newly-uploaded image from the `Choose Antibody Media Files` window.

* Click `Submit Data` to link your image or PDF to the antibody test. Note you may need to refresh the page to see the results.


<div class="page-break"></div>

<a name="copy"/>
<!--
## 6. Add additional tests by copying

If you've done several tests that are mostly the same (e.g., two tests that differ only by media type and outcome), you can save time by copying an existing test and modifying it.

* Start at the record you want to copy.

* Click `Copy` at the top of the page (if you don't see the `Copy` button, you're probably not logged in).

![Screenshot of the Copy button](wiki_images/submitting-data/antibody-test-example-base-copy.png)

* Make the desired changes to the new record and click the `Submit Data` button.
-->

## 6. Reviewing and Submitting Antibody Data

**Note: By the hard launch of the new GUDMAP site in April, there will be dashboards and email notifications to make this process more straightforward. In the meantime, here is how a project's PI or designated reviewer can find their project's data with a Curation Status of "PI Review"**

* Make sure you are logged in.

* From the navigation bar, click _Search > Antibody Data > Antibody Tests_.
    
* In the faceting sidebar on the left, scroll to **Curation Status** and choose _PI Review_. Note: Keep in mind that the data submitter may have forgotten to set the Curation Status field, in which case the status would still be _In Preparation_.

* In the faceting sidebar, scroll to **Principal Investigator** and choose your project's PI. Now you should see the data you need to review.

* When your record is approved internally, change _Curation Status_ to _Submitted_ to send it to the Hub (click here for the full [Curation Workflow](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Curation-Workflow)).

## 7. Deleting Antibody Data

Before you can delete Antibody Test record, you must delete (unlink) any distributions, test summary sheets  or test images associated with it. 

To delete an antibody test record:

* In the 'Distributions' field, click the Edit link to the right and for each distribution, click the 'x' icon in the _Actions_ column.

* Scroll down the record to the sections for 'Test Summary Sheets' and 'Test Images'.
* In each of these sections, unlink the entries by clicking the 'x' icon in the _Actions_ columns.

* Once all of the related records have been deleted (unlinked), then scroll up to the top of the record and click _Delete_.

![Delete button](wiki_images/submitting-data/chaise-delete-option.png)
