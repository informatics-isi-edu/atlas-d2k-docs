---
title: Submitting Protocols
permalink: /docs/protocols/
---

<!-- uncomment when generating PDF in Atom -->
<!-- comment out when generating PDF in Atom
**[PDF version](/docs/protocols.pdf)**
-->
This page provides instructions for adding protocols to the ATLAS-D2K Data Explorer, based on the _Nature Protocols_ format.

If you have any questions or feedback, please send them to your consortium's help email: [help@atlas-d2k.org](mailto:help@atlas-d2k.org).

We also have the following training materials available:
* [Webinar Slides](/assets/slides/GUDMAP-RBK-12062017-data_submission_workshop-protocols-final.pptx)
* [Webinar Replay 12/6/17 (41:12)](https://youtu.be/n-Z8O-ldoyk)
* Tutorial Videos (Coming Soon)


<a name="schema"/>

## Schema

![Diagram of protocol model](/assets/wiki_images/submitting-data/protocol-schema.png)

<div class="page-break"></div>


<a name="overview"/>

## Overview

Adding protocols involves the following steps:

1. Make sure you are in the correct Globus authentication group.
2. Create a base Protocol record (Required).
3. Add at least one Subject Term (Required)
4. Add at least one Keyword (Required)
5. Add at least one contact Protocol Authors (Required)
6. Add Figures, Videos (Optional)
7. If a protocol needs updating, create a new one and update the _Version_ field


<a name="globus"/>

## 1. Join the correct group

[Follow the instructions on this page](accessing-gudmap-and-rbk-resources/). If you're not sure which group you need to join, please contact [help@atlas-d2k.org](help@atlas-d2k.org).

<a name="base-record"/>

## 1. Create the base Protocol Record

* Make sure you are logged in.

* In the top navigation bar, click _Create > Protocol > Protocols_.

    ![Screenshot of navigating to create protocols](/assets/wiki_images/submitting-data/create-protocols-nav.png)

<div class="page-break"></div>

* The _Create Protocols Record_ form appears (see excerpt below):

    ![Screenshot of navigating to create protocols](/assets/wiki_images/submitting-data/create-protocols-record-form.png)

    See screenhot of [full length form here](/assets/wiki_images/submitting-data/create-protocols-record-form-full.png).

* Fill in the fields. Note that the following fields are **required**: (You can format text using Markdown. [Find more information about formatting your larger text fields here](/docs/formatting-with-markdown).)

  * _Title_: Please provide a concise but informative title that describes the protocol to unfamiliar users.
  * _Abstract_: Add a short paragraph describing the protocol further
  * _Procedure_: Enter the actual steps to perform the protocol.
  * _Data Provider_: This is your lab's institution. If you need to add an institution, please contact the Hub.
  * _Curation Status_: Choose either
    * _In Preparation_ (still drafting),
    * _PI Review_ (ready for internal approval), or
    * _Submitted_ (ready for Hub review). Your data will **not** be viewable publicly until approved for _Release_ by the Hub. [For a complete description of the Curation Process, click here.](/docs/curation-workflow)
* We encourage you to fill out the _Anticipated Results_ field in your protocol to help users know if it worked as intended.
* When finished, scroll back to the top of the page and click _Submit Data_.

<div class="page-break"></div>

<a name="subjects"/>

## 2. Add Subject Terms

Although only one Subject Term is required for a protocol, we **highly recommend adding two or three** to make your protocol easier to search.

* From the base protocol record you just created, scroll down until you see the section "Protocol Subject"

![Screenshot of related records section](/assets/wiki_images/submitting-data/chaise-record-sections.png)

* Click the `Add` link in the upper right corner of the "Protocol Subject" section.

![Screenshot of related records section](/assets/wiki_images/submitting-data/chaise-record-sections-choose-add.png)

<div class="page-break"></div>

* In the modal window, scroll through the list or start typing a term in the search box to narrow the results.

![Screenshot of related records section](/assets/wiki_images/submitting-data/chaise-search-and-select.png)

* Click the checkboxes of your desired subject terms.

* When finished, click _Submit_ in the upper right corner to save your data.

* Repeat for each subject term you wish to add.

* You can always navigate back to the record and click _Edit_ and make changes to your record.

![Screenshot of Edit link in records header](/assets/wiki_images/submitting-data/chaise-edit-option.png)

<div class="page-break"></div>

<a name="keywords"/>

## 3. Add Keywords

The process for adding Keywords is basically the same as for Subject Terms.

Although only one Keyword is required for a protocol, we **highly recommend adding two or three** to make your protocol easier to search.

* If you need **to add a keyword, send email to Todd Valerius** at [todd@valeriuslab.org](mailto:todd@valeriuslab.org). Please make sure you've searched the existing list before requesting a new term.

* From the base protocol record, scroll down until you see the section "Protocol Keyword"

![Screenshot of related records section](/assets/wiki_images/submitting-data/chaise-record-sections-key.png)

* Click the `Add` link in the upper right corner of the "Protocol Keyword" section.

![Screenshot of related records section](/assets/wiki_images/submitting-data/chaise-record-sections-choose-add-keywords.png)

<div class="page-break"></div>

* In the modal window, scroll through the list...  

![Screenshot of search and select window](/assets/wiki_images/submitting-data/chaise-search-and-select-keywords.png)

OR

...start typing a term in the search box to narrow the results.

![Screenshot of search and select window](/assets/wiki_images/submitting-data/search-keyword.png)

* Click the checkboxes of your desired keywords.

* When finished, click _Submit_ in the upper right corner to save your data.

![Screenshot of submit button](/assets/wiki_images/submitting-data/search-and-select-submit.png)

* Note that until you change the _Curation Status_ field to _Submitted_, you can keep going back to a record to edit and submit (save) as much as you like.

<div class="page-break"></div>

<a name="authors"/>

### 4. Add Protocol Authors

* From your new protocol record, scroll down until you see the section "Protocol Authors".

![Screenshot of related records section](/assets/wiki_images/submitting-data/chaise-record-sections-authors.png)

* Click the `Add` link in the upper right corner of the "Protocol Authors" section.

![Screenshot of related records section](/assets/wiki_images/submitting-data/chaise-record-sections-author-add.png)

<div class="page-break"></div>

The 'Create Protocol Author Record' tab appears.

![Screenshot of related records section](/assets/wiki_images/submitting-data/chaise-create-author-record.png)

* Fill out the fields.

![Screenshot of related records section](/assets/wiki_images/submitting-data/chaise-create-author-record-req-fields.png)

* In the _Correspondence Author_ field, select 'false' or 'true' to indicate whether this author is the contact person for this protocol.

* In the _Author_ field, click "Select a value". In the modal window (next image), Search for the person you want to add and select them.

![Screenshot of related records section](/assets/wiki_images/submitting-data/chaise-choose-person.png)

* If you cannot find the author, click the "+" button to create a new author record.

![Screenshot of related records section](/assets/wiki_images/submitting-data/chaise-add-person.png)

<div class="page-break"></div>

A "Create Person Record' tab appears.

![Screenshot of related records section](/assets/wiki_images/submitting-data/chaise-create-person-record.png)

- Add the author's full name and email address at the minimum.
- Click **Submit Data**. Close this tab.
- In the previous tab and click the checkbox to select the new author, and click **Submit Data**.

<div class="page-break"></div>

<a name="figures"/>

## 5. Add Figures

Note: The 'Figures' section was primarily intended for adding images to a protocol but is also useful for videos or other supplemental files. For simplicity, we'll refer to image files below.

The process of adding image files to a protocol is two-fold: you add the file to the _Figures_ section and then embed it where desired in the base protocol.

* Make sure you are logged in, then navigate to the protocol where you want to add the figure (in the navigation bar, click _Search > Protocol > Protocol_).

![Screenshot of using navbar to search histological slides](/assets/wiki_images/submitting-data/search-protocol-nav.png)

* Scroll down to the _Figures_ section and click `Add`. A new tab appears with a form.

![Screenshot of clicking to add a figure](/assets/wiki_images/submitting-data/chaise-record-add-figures.png)

<div class="page-break"></div>

* Fill in the fields and then upload your figure in the _URI_ field by clicking **Submit File**, navigating to your file and clicking **Open**.

![Screenshot of clicking to upload a figure file](/assets/wiki_images/submitting-data/chaise-record-upload-figures.png)

* Save the record by clicking _Submit Data_. Your figure now appears in the _Figures_ section.

<div class="page-break"></div>

<a name="embed"/>

### 6. Embed Figure in the Protocol

Note you can only embed an image file. For video files, you may only add a link to the URI for the figure (for information on how to add a link, see [Formatting with Markdown](/docs/formatting-with-markdown)).

* In the _Figures_ section, copy the _URI_ field (the link to the image on our system).

![Screenshot displaying where to copy the URI](/assets/wiki_images/submitting-data/chaise-copy-uri.png)

* Scroll back up to the top of the protocol and click **Edit**.

![Screenshot of Edit link in record header](/assets/wiki_images/submitting-data/chaise-edit-option.png)

<div class="page-break"></div>

* In the desired field, use the following Markdown format (similar to a markdown link but with an exclamation point at the beginning):

`![alt text](URI-of-image-you-uploaded)`

![Example of Markdown markup for embedding a figure](/assets/wiki_images/submitting-data/chaise-record-embed-figures.png)

You can also click the Images icon in the formatting toolbar and paste the URL in the popup window.

![Example of Images icon for embedding a figure](/assets/wiki_images/submitting-data/chaise-images-icon.png)

* Your figure now appears in the text field.

![Results of markup](/assets/wiki_images/submitting-data/chaise-record-figure-appears.png)

<div class="page-break"></div>

<a name="reviewing"/>

## 7. Reviewing and Submitting Protocols

**Note: Here is how a project's PI or designated reviewer can find their project's data with a Curation Status of "PI Review"**

* Make sure you are logged in.

* From the navigation bar, click _Search > Protocol > Protocols_.

* In the faceting sidebar on the left, scroll to **Curation Status** and choose _PI Review_. Note: Keep in mind that the data submitter may have forgotten to set the Curation Status field, in which case the status would still be _In Preparation_.

* In the faceting sidebar, scroll to **Principal Investigator** and choose your project's PI. Now you should see the data you need to review.

* When your record is approved internally, change _Curation Status_ to _Submitted_ to send it to the Hub (click here for the full [Curation Workflow](/docs/curation-workflow)). It's a good idea to also send email to the Hub to let them know your protocol has been submitted (help@gudmap.org or help@rebuildingakidney.org).


<div class="page-break"></div>

<a name="versioning"/>

## 8. Versions of Protocols

Sometimes a protocol needs to be updated due to things like cheaper reagents or better processes.

Protocols include a _Version_ field to help distinguish between these. Here are some guidelines for using this field.

If the investigator feels their protocol is a significant difference from the original, AND data on the ATLAS-D2K website that links to the protocol cannot be replicated with the old version, create a brand new protocol and update the _Version_ field by one "whole" number (ie, from "1" to "2").

If you only need to add a clarification or a note, or if a reagent source is substituted that does not change the outcome of the protocol (but saves money, for example), then edit the existing protocol and update the _Version_ field by a "point" number, (ie, from "1" to "1.1").

Investigators are responsible for determining title changes when a protocol changes. If you are moving a whole number (the first case above), we recommend updating the title to better reflect the change.

<a name="deleting"/>

## 9. Deleting Protocols

Before you can delete a protocol, you must first unlink (delete) any records associated with it. This means 'un-linking' the keywords, subject terms and authors.

* First, make sure you navigate to the protocol you wish to delete and are logged in.

* Scroll down below the base protocol until you see the 'Protocol Subject', 'Protocol Keywords', 'Protocol Authors' and 'Figures' sections.

![Records sections](/assets/wiki_images/submitting-data/chaise-record-sections.png)

* For the 'Protocol Subject' and 'Protocol Keywords' sections, click _Edit_ in the upper right corner of the section.

    ![Choose Edit](/assets/wiki_images/submitting-data/chaise-record-sections-choose-edit.png)

    Then click the "x" icon in the Actions columns to delete (un-link) each and every record in that section.

    ![Un-link Subject](/assets/wiki_images/submitting-data/chaise-record-sections-unlink-subject.png)

* For the 'Protocol Authors' and 'Figures' sections, click the 'garbage can' icon to delete each and every record in that section.

![Delete authors](/assets/wiki_images/submitting-data/chaise-record-sections-unlink-authors.png)

* Once all of the related records are deleted, scroll back up to the top of the protocol and click the "Delete" link.

![Delete base protocol](/assets/wiki_images/submitting-data/chaise-delete-option.png)
