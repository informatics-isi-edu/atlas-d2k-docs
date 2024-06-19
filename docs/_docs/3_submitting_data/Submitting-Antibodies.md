---
title: Submitting Antibodies
permalink: /docs/antibodies/
---


This page provides instructions for adding antibody validation data to the ATLAS-D2K Data Explorer.

If you have any questions or feedback, please send them to your consortium's help email: [help@atlas-d2k.org](mailto:help@atlas-d2k.org)

We also have the following training materials available (Note that these are from 2017 and there have been many changes to the UI. But the concepts are generally the same.):
* [Webinar Slides]({{ "/assets/slides/GUDMAP-RBK-12112017-data_submission_workshop-antibodies.pptx?raw=true" | relative_url }})
* [Webinar Replay 12/11/2017 (37:08)](https://youtu.be/3bQMSogtVY4)

## Overview

Adding antibody validation data involves the following steps:

* Make sure you are in the correct Globus authentication group ([follow the instructions on this page](../accessing-gudmap-and-rbk-resources/)), and that you are logged in.
* Search that antibody data already exists for your test.
* If it doesn't, then create an antibody record.
* Create an antibody test record.
* Add distribution terms to your antibody test record.
* Add any images or other media.
* Add a test summary sheet.
* You may also 'bulk add' several test records if they are similar (ie, only the media type and outcome are different).

<a name="schema"/>

## Schema

![Antibody schema diagram]({{ "/assets/wiki_images/submitting-data/antibody_schema.jpg" | relative_url }})

The Antibody schema contains two main tables:
* Antibodies: General product information about each antibody, similar to what might be found on the manufacturer's website.
* Antibody Tests: Information about researchers' experience using each antibody.

Other related tables include:
* Antibody Media Files: Images and other media files related to antibody tests (slide images, summary PDFs, etc.)
* Test Methods: Descriptions of the methods used in antibody tests.
* Various vocabulary tables.

<a name="globus"/>

## 0. Are you in the correct group? (Required)

[Follow the instructions on this page](../accessing-gudmap-and-rbk-resources/). If you're not sure which group you need to join, please contact [help@atlas-d2k.org](mailto:help@atlas-d2k.org).

<a name="search-antibody"/>

## 1. Search for the antibody you're working on

* Go to [https://www.atlas-d2k.org/chaise/recordset/#2/Antibody:Antibodies](https://www.atlas-d2k.org/chaise/recordset/#2/Antibody:Antibodies) and log in.

* This will take you to the antibody search page, which you can use to find out if the antibody you're working on is already listed in our database. Start typing the name of the antibody in the search field or use the filtering sidebar on the left to narrow down the results.
<!--
![Screenshot of antibodies search page]({{ "/assets/wiki_images/submitting-data/antibody-search-page.png" | relative_url }})
-->

* If your antibody is there, you can go ahead and create the antibody test record (See next section). If not, move on to the next step below.

<a name="create-antibody"/>

## 2. If you cannot find the antibody, create a new antibody record

If you did find the antibody, move on to the next step.

* Click the `+Create` button. (If you are not on the Antibodies page, from the navigation bar, click _Internal > Antibodies > Antibody Listing_.)

  The `Create Antibodies Record` form opens in a new browser tab.
<!--
  ![Screenshot of the Create Antibodies form]({{ "/assets/wiki_images/submitting-data/create-antibody.png" | relative_url }})
-->
* Select the values for each relevant field. The **required** fields are:
  * _Company ID_
  * _Catalog Number_
  * _Curation Status_: Choose either
    * _In Preparation_ (still drafting) or
    * _Submitted_ (ready for Hub review). Your data will **not** be viewable publicly until approved for _Release_ by the Hub. [For a complete description of the Curation Process, click here.](../curation-workflow)
  * _Consortium_

* When finished, click `Save` to save your new antibody record. You can now close this tab.

### What if my antibody is not from a vendor?

If your antibody is not from a vendor (ie, it's a donated reagent), then you may choose a name for the _Company ID_ ("Donated reagent from X Lab") and use the RRID for the _Catalog Number_ or some other unique identifier.

<a name="create-antibody-test"/>

## 3. Create your new antibody test record

* From the navigation bar, click _Internal > Antibodies > Antibody Validation_.

    The `Create Antibody Tests Record` form appears.
<!--
    ![Screenshot of the Create Antibody Test Record form]({{ "/assets/wiki_images/submitting-data/create-antibody-test.png" | relative_url }})
-->
* Select the values for each relevant field. The required fields are:
  * _Antibody Product ID_
  * _Protein Target_: Note that this list comes from the NCBI Gene List and should include all proteins. Also, you will soon be able to search on synonyms.
  * _Curation Status_: Choose either
    * _In Preparation_ (still drafting),
    * _Submitted_ (ready for Hub review). Your data will **not** be viewable publicly until approved for _Release_ by the Hub. [For a complete description of the Curation Process, click here.](/docs/curation-workflow)
  * _Principal Investigator_: Choose the name of your project's contact PI.
  * _Consortium_

* Note: If you are creating multiple antibody test records, you may click the `Clone` button (under the `Save` button) to copy over the record form. Each time you click `Clone` will display a copy of the most recent form that you can edit as needed. You can also add a number to the `Qty` field to clone more than one record at a time.

* When finished, click `Save` to save your new antibody test record(s).

* If you are not finished with your submission, you may still save your work by clicking the `Save` button. Then you may go back to the record, log in and click `Edit` to resume filling it out.
<!--
![Screenshot of the Edit button]({{ "/assets/wiki_images/submitting-data/general-record-header-edit.png" | relative_url }})
-->

<a name="distribution"/>

## 4. Add Expression Region terms to your antibody test record

* Scroll down the antibody test record until you see a section labelled `Expression Region`. This is our term for cell types / anatomical regions relevant to this antibody test.

* Click `Link Records` in the `Expression Region` section.
<!--
![Screenshot pointing out the Add link in the Distribution section]({{ "/assets/wiki_images/submitting-data/antibody-test-example-distribution-add.png" | relative_url }})
-->
  This will bring up a `Create Antibody Test Distribution Record` window.

* Start typing the anatomical term in the search term to narrow your results.
<!--
![Screenshot of searching for distribution terms]({{ "/assets/wiki_images/submitting-data/antibody-test-example-distribution-search.png" | relative_url }})
-->
* Click `Select a value`
* Click the checkmark to the left of your desired distribution value.
* Click `Save` to add the distribution.
* Repeat for as many distributions as desired.

<a name="test-results"/>

## 5. Add test summary sheets and images

Near the bottom of the newly-created antibody test record, you'll see empty sections labelled `Test Summary Sheets` for PDF summaries of the test, and `Antibody Test Images` for slide images relevant to the test.
<!--
![Screenshot of Test Summary Sheets and Test Images sections]({{ "/assets/wiki_images/submitting-data/antibody-test-example-media-files-sections.png" | relative_url }})
-->

To add a test-related files:

* Click `Link Records` in the `Test Summary Sheets` or `Test Images`.
<!--
![Screenshot of Add links]({{ "/assets/wiki_images/submitting-data/antibody-test-example-files-add.png" | relative_url }})
-->
  This will bring up the `Link Antibody Media Files...` window.
<!--
![Screenshot of the Choose Antibody Media Files window]({{ "/assets/wiki_images/submitting-data/antibody-choose-media-files.png" | relative_url }})
-->
* If the desired file has already been uploaded, select it.

* If not, upload your file:

    * Click the `+ Create new` button towards the top-right of the window.

    This will open the `Create Antibody Media Files Record` page in a separate browser tab.
<!--
    ![Screenshot of the Create Antibody Media Files window]({{ "/assets/wiki_images/submitting-data/antibody-create-media-files.png" | relative_url }})
-->
    * Click on `Select File` to select a file from your computer. (Either an image file if you're adding a test image or a PDF for the test summary).

* Please use the _Description_ Field to paste in the summary of the test result doc from the PDF.    
* Fill in the rest of the fields on the form. Required fields are:
      * _Media Type_
      * _Curation Status_: Choose either
        * _In Preparation_ (still drafting),
        * _Submitted_ (ready for Hub review). Your data will **not** be viewable publicly until approved for _Release_ by the Hub. [For a complete description of the Curation Process, click here.](../curation-workflow)
      * _Principal Investigator_: Choose the name of the contact PI for your project. If their name isn't available, please contact the Hub.
      * _Consortium_: Make sure you indicate whether this is from the ATLAS-D2K consortium.

* Click `Save` to complete the upload.

* Go back to the browser tab of your Antibody Test Record and select your newly-uploaded image from the `Choose Antibody Media Files` window.

* Click `Save` to link your image or PDF to the antibody test. Note you may need to refresh the page to see the results.

<!--
<a name="copy"/>

## 6. Add additional tests by copying

If you've done several tests that are mostly the same (e.g., two tests that differ only by media type and outcome), you can save time by copying an existing test and modifying it.

* Start at the record you want to copy.

* Click `Copy` at the top of the page (if you don't see the `Copy` button, you're probably not logged in).

![Screenshot of the Copy button]({{ "/assets/wiki_images/submitting-data/antibody-test-example-base-copy.png" | relative_url }})

* Make the desired changes to the new record and click the `Save` button.
-->

## 6. Reviewing and Submitting Antibody Data

* Make sure you are logged in.

* From the navigation bar, click _Data > Antibodies > Antibody Validation_.

* In the faceting sidebar on the left, scroll to **Principal Investigator** and search for the project's PI name. The newest records should appear at the top.

* When your record is approved internally, change _Curation Status_ to _Submitted_ to send it to the Hub (click here for the full [Curation Workflow](../curation-workflow)).
