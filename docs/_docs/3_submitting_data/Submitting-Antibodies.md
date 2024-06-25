---
title: Submitting Antibodies
permalink: /docs/antibodies/
---


This page provides instructions for adding antibody validation data to the ATLAS-D2K Data Explorer. Antibody Tests (sometimes referred to as "Antibody Validation") are specific comparisons of antibody performance on a tissue (e.g. human/mouse) with various fixation methods (e.g. frozen/paraffin). The results may help researchers select suitable antibodies for their work.

If you have any questions or feedback, please send them to your consortium's help email: [help@atlas-d2k.org](mailto:help@atlas-d2k.org)

## Table of Contents

## Table of Contents

- [Metadata Model for Antibodies and Antibody Tests](#metadata-model-for-antibodies-and-antibody-tests)
- [1. Joining the Globus Group](#1-joining-the-globus-group)
- [2. Overview of adding Antibody Tests](#2-overview-of-adding-antibody-tests)
- [3. Search for the antibody you're working on](#3-search-for-the-antibody-youre-working-on)
  - [3.1 If your test involved *lectin*](#31-if-your-test-involved-lectin)
- [4. If you cannot find the antibody, create a new Antibody record](#4-if-you-cannot-find-the-antibody-create-a-new-antibody-record)
  - [4.1 Fields for Antibody records](#41-fields-for-antibody-records)
  - [4.2 What if my antibody is not from a vendor?](#42-what-if-my-antibody-is-not-from-a-vendor)
- [5. Create an Antibody Test record](#5-create-an-antibody-test-record)
  - [5.1 Fields for Antibody Test record](#51-fields-for-antibody-test-record)
- [6. Add Test Summary Sheets and Antibody Test Images](#6-add-test-summary-sheets-and-antibody-test-images)
  - [6.1 Fields for Antibody Media File record](#61-fields-for-antibody-media-file-record)
- [7. Add Antibody Test Distribution terms](#7-add-antibody-test-distribution-terms)
- [8. Reviewing and Submitting Antibody Data](#8-reviewing-and-submitting-antibody-data)


## Metadata Model for Antibodies and Antibody Tests

![Antibody schema diagram]({{ "/assets/wiki_images/submitting-data/antibody_schema.jpg" | relative_url }})

The Antibody schema contains two main tables:
* Antibodies: General product information about each antibody, similar to what might be found on the manufacturer's website.
* Antibody Tests: Information about researchers' experience using each antibody.

Other related tables include:
* Antibody Media Files: Images and other media files related to antibody tests (slide images, summary PDFs, etc.)
* Test Methods: Descriptions of the methods used in antibody tests.
* Various vocabulary tables.

## 1. Joining the Globus Group

To get editing access, join the relevant Globus group. Email [help@atlas-d2k.org](mailto:help@atlas-d2k.org) for assistance. For detailed information, see [Accessing ATLAS-D2K Resources](../accessing-atlas-resources/).

## 2. Overview of adding Antibody Tests

Adding antibody validation data involves the following steps:

* [Search](#3-search-for-the-antibody-youre-working-on) to see if the antibody for your test is already listed in our catalog.
* If you cannot find the antibody, [create an Antibody record](#4-if-you-cannot-find-the-antibody-create-a-new-antibody-record).
* [Create an Antibody Test record.](#5-create-an-antibody-test-record)
* [Add a Test Summary Sheet or Antibody Test Images.](#6-add-test-summary-sheets-and-antibody-test-images) This is where you upload the PDFs and images that show the results of the test.
* [Add Antibody Distribution terms](#7-add-antibody-test-distribution-terms) to your antibody test record. These are the anatomical/cell type regions involved in your test.

Note: You may also ["bulk add" or "clone"](../advanced-editing-features/) several test records if they are similar (ie, only the media type and outcome are different).

## 3. Search for the antibody you're working on

* Go to [https://www.atlas-d2k.org/chaise/recordset/#2/Antibody:Antibodies](https://www.atlas-d2k.org/chaise/recordset/#2/Antibody:Antibodies) and log in.

* This will take you to the antibody search page, which you can use to find out if the antibody you're working on is already listed in our database. Start typing the name of the antibody in the search field or use the filtering sidebar on the left to narrow down the results.

![Screenshot of antibodies search page]({{ "/assets/wiki_images/submitting-data/antibody-search-page.png" | relative_url }})

* If your antibody is there, go ahead and create the Antibody Test [See Section 5 below](#5-create-an-antibody-test-record). If not, move on to the next step below (section 4).

### 3.1 If your test involved *lectin*

Although *lectin* is not an antibody, the system treats it as one because most of the principles are the same.

## 4. If you cannot find the antibody, create a new Antibody record

If you did not find the antibody in our listings:

* Click the `Create` button. (If you are not on the Antibodies page, from the navigation bar, click _Internal > Antibodies > Antibody Listing_.)

  The `Create Antibodies Record` form opens in a new browser tab.

  ![Screenshot of the Create Antibodies form]({{ "/assets/wiki_images/submitting-data/create-antibody.png" | relative_url }})

* Select the values for each relevant field.

### 4.1 Fields for Antibody records

<table>
   <tr>
      <th>Field</th>
      <th>Description</th>
      <th>Required or Optional</th>
   </tr>
   <tr>
      <td class="required">Company ID</td>
      <td>TBD</td>
      <td class="required">Required</td>
   </tr>
   <tr>
      <td class="required">Catalog Number</td>
      <td>TBD</td>
      <td class="required">Required</td>
   </tr>
   <tr>
      <td>Host Species</td>
      <td>The species from which this antibody was derived.</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Host Monoclonal</td>
      <td>Select true if this antibody is monoclonal.</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Product Name</td>
      <td>The product name of this antibody.</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>RRID</td>
      <td>Research Resource IDentifier of this antibody.</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Clone ID</td>
      <td>TBD</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Production Method</td>
      <td>TBD</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Immunoglobin Isotype</td>
      <td>TBD</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Purification Method</td>
      <td>You can link to the related protocol.</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Direct Label</td>
      <td>TBD</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Variant Type</td>
      <td>TBD</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Variant Name</td>
      <td>TBD</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Notes</td>
      <td>Use this text field for your own notes that you wish to add.</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td class="required">Curation Status</td>
      <td>Indicates if this record is still being worked on, is being reviewed, is embargoed until publication or has been released to the public. For a complete description of the curation process, see <a href="../curation-workflow/">Curation Workflow</a></td>
      <td class="required">Required</td>
   </tr>
   <tr>
      <td class="required">Principal Investigator</td>
      <td>Use the primary Principal Investigator for this collection of data. You may only indicate one PI.</td>
      <td class="required">Required</td>
   </tr>
   <tr>
      <td class="required">Consortium</td>
      <td>Indicate the Consortium (GUDMAP or RBK).</td>
      <td class="required">Required</td>
   </tr>
</table>

* When finished, click `Save` to save your new antibody record.

### 4.2 What if my antibody is not from a vendor?

If your antibody is not from a vendor (ie, it's a donated reagent), then you may choose a name for the _Company ID_ ("Donated reagent from X Lab") and use the RRID for the _Catalog Number_ or some other unique identifier.


## 5. Create an Antibody Test record

Once the relevant Antibody records are in our listing, create the Antibody Test record:

* From the navigation bar, click _Internal > Antibodies > Antibody Validation_.

    The `Create Antibody Tests Record` form appears.

    ![Screenshot of the Create Antibody Test Record form]({{ "/assets/wiki_images/submitting-data/create-antibody-test.png" | relative_url }})

* Select the values for each relevant field. See section 5.1 below.

* Note: If you are creating multiple antibody test records, you may click the `Clone` button (under the `Save` button) to copy over the record form. Each time you click `Clone` will display a copy of the most recent form that you can edit as needed. You can also add a number to the `Qty` field to clone more than one record at a time.

* When finished, click `Save` to save your new antibody test record(s).

### 5.1 Fields for Antibody Test record

<table>
   <tr>
      <th>Field</th>
      <th>Description</th>
      <th>Required or Optional</th>
   </tr>
   <tr>
      <td class="required">Antibody Product ID</td>
      <td>The product ID of the antibody used in this test.</td>
      <td class="required">Required</td>
   </tr>
   <tr>
      <td>Species Tested In</td>
      <td>The species of the organism used in this test.</td>
      <td>Required</td>
   </tr>
   <tr>
      <td>Stage</td>
      <td>The developmental stage of the organism used in this test.</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Protein Target</td>
      <td>The protein targeted in this test.</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Comments</td>
      <td>Use this field to add any comments related to this test.</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Cost</td>
      <td>The cost of the antibody used in this test.</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Medium</td>
      <td>The slide preparation used (frozen or paraffin) in this test.</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Expected Detected</td>
      <td>Choose true if the expected antibody binding occurred in this test.</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Additional Detected</td>
      <td>Choose true if additional antibody binding occurred in this test.</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Background Detected</td>
      <td>Choose true if background antibody binding occurred in this test.</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Usability</td>
      <td>Specific detection of the target protein determined to be achieved.</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Working Dilution</td>
      <td>The antibody dilution used in this test.</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Test Method</td>
      <td>Choose the method used in this test.</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td>Lower Titration Possible</td>
      <td>Choose true if the antibody in this test might be usable at a lower concentration through titration.</td>
      <td>Optional</td>
   </tr>
   <tr>
      <td class="required">Curation Status</td>
      <td>Indicates if this record is still being worked on, is being reviewed, is embargoed until publication or has been released to the public. For a complete description of the curation process, see <a href="../curation-workflow/">Curation Workflow</a></td>
      <td class="required">Required</td>
   </tr>
   <tr>
      <td class="required">Principal Investigator</td>
      <td>Use the primary Principal Investigator for this collection of data. You may only indicate one PI.</td>
      <td class="required">Required</td>
   </tr>
   <tr>
      <td class="required">Consortium</td>
      <td>Indicate the Consortium (GUDMAP or RBK).</td>
      <td class="required">Required</td>
   </tr>
</table>

Once you have saved the form, you will see a new Antibody Test record.

**You can come back at any time and click "Edit" in the record header to modify this record.**


## 6. Add Test Summary Sheets and Antibody Test Images

On your new Antibody Test, there are sections labelled `Test Summary Sheets` for PDF summaries of the test, and `Antibody Test Images` for slide images relevant to the test.

![Screenshot that focuses on various sections available on the Antibody Test record]({{ "/assets/wiki_images/submitting-data/antibody-test-sections.png" | relative_url }})

To fill out these sections, you will link to Antibody Media images and upload your media:

* Click `Link Records`.

  This will bring up the `Link Antibody Media Files...` window.

* If the desired file has previously been uploaded, search for and select it.

* If not, upload your file by doing the following:

    * Click the `Create new` button towards the top-right of the window.

    This will open the `Create Antibody Media Files Record` page in a separate browser tab.

    ![Screenshot of the Create Antibody Media Files window]({{ "/assets/wiki_images/submitting-data/antibody-create-media-files.png" | relative_url }})

    * Click on `Select File` to select a file from your computer. (Either an image file if you're adding a test image or a PDF for the test summary).

### 6.1 Fields for Antibody Media File record

<table>
<tr>
   <td>Thumbnail Image</td>
   <td>Choose a file TBD</td>
   <td>Optional</td>
</tr>
<tr>
   <td class="required">File</td>
   <td>Select the relevant media file.</td>
   <td class="required">Required</td>
</tr>
<tr>
   <td class="required">Media Type</td>
   <td>Select type of media you are uploading (ie, PDF, JPG, etc).</td>
   <td class="required">Required</td>
</tr>
<tr>
   <td>Description</td>
   <td>For Test Summary Sheets, it would be helpful to paste in the summary of the test result doc from the PDF.</td>
   <td>Optional</td>
</tr>
<tr>
   <td class="required">Curation Status</td>
   <td>Indicates if this record is still being worked on, is being reviewed, is embargoed until publication or has been released to the public. For a complete description of the curation process, see <a href="../curation-workflow/">Curation Workflow</a></td>
   <td class="required">Required</td>
</tr>
<tr>
   <td class="required">Principal Investigator</td>
   <td>Use the primary Principal Investigator for this collection of data. You may only indicate one PI.</td>
   <td class="required">Required</td>
</tr>
<tr>
   <td class="required">Consortium</td>
   <td>Indicate the Consortium (GUDMAP or RBK).</td>
   <td class="required">Required</td>
</tr>
</table>

* Click `Save` to complete the upload and save the media record. You may close this tab.

* Go back to the browser tab of your Antibody Test Record and select your newly-uploaded file from the `Choose Antibody Media Files` window.

* Click `Save` to link your image or PDF to the antibody test. Note: You may need to refresh the page to see the results.

## 7. Add Antibody Test Distribution terms

The _Antibody Test Distribution_ section is where you will add cell types / anatomical regions relevant to this antibody test.

* Click `Add Records`. This will bring up a "Create Antibody Test Distribution record" window.
* Click the **Distribution** field. In the search field, and start typing the anatomical or cell type term to narrow your results.
* Click `Save` to add the distribution.
* Repeat for as many distributions as needed.

If you cannot find the term you need, please contact [help@atlas-d2k.org](mailto:help@atlas-d2k.org).

## 8. Reviewing and Submitting Antibody Data

* Make sure you are logged in.

* From the navigation bar, click _Data > Antibodies > Antibody Validation_.

* In the faceting sidebar on the left, scroll to **Principal Investigator** and search for the project's PI name. The newest records should appear at the top.

* When your record is approved internally, change _Curation Status_ to _Submitted_ to send it to the Hub (click here for the full [Curation Workflow](../curation-workflow)).
