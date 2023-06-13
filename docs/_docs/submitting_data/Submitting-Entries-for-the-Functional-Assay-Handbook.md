Submitting Entries for the Functional Assay Handbook

## Requirement:

* You must have editing access via the **kidney-writers** group. If you are not already a member, please [join the **kidney-writers** group](https://app.globus.org/groups/af0b4010-5b75-11e6-9575-22000aef184d/about) group using this link. Choose to sign in via your institution (use the dropdown list), Google or ORCID and then follow the prompts. When you get to the kidney-writers page, click to **Join this group** button and I’ll approve ASAP.

## Overview

You are actually creating and connecting two types of records:

* the **Functional Assay Handbook** record, which populates the Handbook search with helpful information about targets and requirements for functional assays to help labs determine which assays are the best fit for their experiments and resources.

* the **Protocol** record, which is a standalone record with everything needed to reproduce a protocol and with the proper citations/authors and version number.

In the instructions below, we walk you through creating the Functional Assay record for the Handbook. If the protocol has not already been added to the system, we also describe the process for creating a protocol.

(You may also choose to create the Protocol record first and then create the Functional Assay Handbook record.)

We are still developing this documentation. If you have any questions, please reach out to [help@rebuildingakidney.org](mailto:help@rebuildingakidney.org).

## Step 1: Create base Functional Assay record

First you must create the base record which is a container for all data related and linked to this functional assay record.

* Go to the Functional Assay Handbook page and log in: [https://www.rebuildingakidney.org/chaise/recordset/#2/Protocol:Functional_Assay_Handbook](https://www.rebuildingakidney.org/chaise/recordset/#2/Protocol:Functional_Assay_Handbook)

* Click the **Create** button.

* Fill out the fields. Some notes:

    * *Version*: Please keep this the default and do not edit it.

    * *Curation Status*: Keep **In Preparation** while working on this assay. Then change to **Release** when it’s ready to be viewed by the public.

* When finished, click the **Save** button towards the top of the page.

## Step 2: Link Kidney Structure

From the base record, look for the *Kidney Structure* field and click the **Link records** button. The intent is to focus on the major, higher-level structures instead of sub-segments.

Choose the structure from the anatomy terms. In the future, the Hub will narrow this list to those specifically appropriate for functional assays.

Until then, **please refer to this list of term IDs** (search using these ID numbers and look for the corresponding ID under the ID column). You may enter more than one. If you need a structure that is not listed, please contact [help@rebuildingakidney.org](mailto:help@rebuildingakidney.org).

<table>
  <tr>
    <td>Kidney Structure List</td>
    <td>ID</td>
  </tr>
  <tr>
    <td>Glomerulus</td>
    <td>UBERON:0000074</td>
  </tr>
  <tr>
    <td>Proximal tubule</td>
    <td>EMAPA:28281</td>
  </tr>
  <tr>
    <td>Descending limb</td>
    <td>EMAPA:35511</td>
  </tr>
  <tr>
    <td>Thin ascending limb</td>
    <td>EMAPA:35861</td>
  </tr>
  <tr>
    <td>Thick ascending limb</td>
    <td>EMAPA:35512</td>
  </tr>
  <tr>
    <td>Distal convoluted tubule</td>
    <td>EMAPA:28393</td>
  </tr>
  <tr>
    <td>Connecting tubule</td>
    <td>EMAPA:28011</td>
  </tr>
  <tr>
    <td>Cortical collecting duct</td>
    <td>EMAPA:28130</td>
  </tr>
  <tr>
    <td>Medullary collecting duct</td>
    <td>EMAPA:28061</td>
  </tr>
  <tr>
    <td>Vasculature</td>
    <td>EMAPA:28457</td>
  </tr>
  <tr>
    <td>Interstitium</td>
    <td>EMAPA:28518</td>
  </tr>
</table>


## Step 3: Link Technology

From the base record, look for the *Technology* field and click the **Link records** button.

Choose from the list. You may enter more than one.

If you do not see an existing technology that should be there, click **Create New** and fill out the short form to add a new technology term to the list.

## Step 4: Link Protocol

From the base record, scroll down to the *Protocols* section and click the **Link records** button.

Choose from existing protocols or click **Create New** and create the protocol.

Protocols follow a similar pattern to functional assays where you create the base protocol record and then link further records afterwards. See directions in Step 5 below.

## Step 5: Create Protocol (if not created already)

Overview of steps:

1. Note on Version field

2. Create the base Protocol record (Required).

3. Link at least one record each for Subject, Keyword, and Authors (Required)

4. Upload Figures and/or Videos (Optional)

Protocol records are based on the *[Nature Protocols](https://www.nature.com/nprot/for-authors/preparing-your-submission#protocol)* format. Text fields accept [Markdown formatting](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Formatting-with-Markdown).

### Note on Version field

If a protocol needs updating, create a new one and update the Version field.

**Make sure that the Functional Assay Handbook records links to the correct version of a protocol.**

### Create the base Protocol record (Required)

From Step 4 (above), click **Create New**, fill out the appropriate fields and click **Save**.

Note that the following fields are required:

* *Title*: Please provide a concise but informative title that describes the protocol to unfamiliar users.

* *Abstract*: Add a short paragraph describing the protocol further

* *Procedure*: Enter the actual steps to perform the protocol.

* *Data Provider*: This is your lab's institution. If you need to add an institution, please contact the Hub.

* *Principal Investigator*: Choose the contact PI from the list. If not available, contact [help@rebuildingakidney.org](mailto:help@rebuildingakidney.org).

* *Curation Status*: Use **In Preparation** while drafting, but when ready, click **Submit**. Cris from the Hub will review and approve.

**We encourage you to include *Anticipated Results* in your protocol to help users know if it worked as intended.**


### Link records for Subject, Keyword, and Authors (Required)

On the Protocol record you just created, scroll down to each of the following sections and click **Link records** to add at least one of each (but you can add as many as applicable):

* *Protocol Subject*: These are subject categories related to the protocol (per Nature Protocols)

* *Protocol Keyword*: These are just helpful search terms. Either choose from the list or click **Create new** to create your own.

* *Protocol Author*: Click **Add records** for each protocol author. If they’re not already available, click **Create New** to add new people as authors.

Search through existing entries to find the best possible fit. But if you cannot find one, you can click the **Create new** button and make new entries.

### Upload Attachments (for Images, Figures, Videos, etc) (Optional)

This section may be used for adding images to your protocol but is also useful for videos or other supplemental files.

To embed image files in your protocol: add the file to the Attachments section, copy the link and then embed it where desired in the base protocol. **Important: You may only embed image files in .jpg or .png format.**

* Scroll to the *Attachments* section and click **Add records**.

    * Use the *Label* field to describe the attachment.

    * Use the *URI* field to upload the file.

    * Click Save

* Embed Image: Note you can only embed an image file (in .jpg or .png format). For video files, you may only add a link to the URI for the figure (for information on how to add a link, see [Formatting with Markdown](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Formatting-with-Markdown)).

    * In the record you just added, copy the *URI* field (the link to the image on our system).

    * Scroll back up to the top of the protocol and click **Edit**.

    * In the desired field, use the following Markdown format (similar to a markdown link but with an exclamation point at the beginning):

```![alt text](URI-of-image-you-uploaded)```
