---
title: Advanced Editing Features
permalink: /docs/advanced-editing-features/
---

<!-- uncomment when generating PDF in Atom -->
<!-- comment out when generating PDF in Atom 
**[PDF version](/docs/misc/Advanced-Editing-Features.pdf)**
-->

The following are some very useful features of editing in the Data Browser that can make data entry much faster and easier.

- [1. Multi-create](#1-multi-create)
- [2. Multi-edit](#2-multi-edit)
- [3. Copy record](#3-copy-record)
- [4. Bulk uploading your data files](#4-bulk-uploading-your-data-files)


## 1. Multi-create

Whenever you are on any "Create" or "Edit" form, you can click the plus sign or down arrow in the upper right corner to add duplicates of that form. 

![Screenshot of the multi-create buttons](wiki_images/advanced/multi-create-buttons.png)

- The plus sign will add a new record each time you click it.
- The down arrow will let you enter a number of records to create at once. The maximum is 200 records, but it's more manageable to do a smaller number at a time.

You can add many records at a time this way, but depending on the quality of your wireless connection, you might want to keep it to no more than 10 at a time. 

What's especially helpful is that when you click either button, the new entries it generates copies any field values from the last form appearing. This means that you can fill out any common field values (ie, Species, Age Stage, etc) and they will be carried over as you click the plus sign or down arrow. 

Here's a quick video demonstration:

[![Multi-create Demonstration](http://img.youtube.com/vi/CRTEb0Z7sEw/0.jpg)](https://www.youtube.com/watch?v=CRTEb0Z7sEw "Multi-create")

## 2. Multi-edit

You can filter your search to display records that you want to change and edit hte values for the same field across all of the records at the same time. 

To multi-edit:
1. Filter data to pull up a search for the records you want to change.
2. In the record header, click _Edit_. All of the records in the search results are displayed in editing mode. (You will not see this option unless you are logged in.)
3. Find the field you want to change across all of the records and click the pencil icon to the left of the field.
4. Enter the new value and click `Apply All`. You also have the option to `Clear All` or `Cancel` the operation.


Here's an example for editing all of the experiments within a study:

1. In the menu, go to _Search > Gene Expression > Sequencing Data > Studies_.
2. In the **Title** filter (in the lefthand filtering sidebar) type one of the words you know is in the title of the study you want to pull it up. Or use one of the other filters in the sidebar or search field to find a particular Study.
3. Click the eye for that Study to go to its record page. 
4. Scroll down to the Experiments table and click `View More` to the right side of the table:

![Shows 'View more' link for a table](wiki_images/advanced/multi-edit-view-more.png)

This pulls up a search results page for all the Experiments for the study. 

5. Then click `Edit` in the record header:

![Shows 'Edit' link in record header](wiki_images/advanced/multi-edit-records-edit.png)

This puts all of those records into editing mode at the same time. 

6. Click the pencil icon to the left side of a row to add the same field value to all of them:

![Shows 'pencil' link for a field in multi-edit mode](wiki_images/advanced/multi-edit-records-edit-pencil.png)

<div class="page-break"></div>

## 3. Copy record

Another useful feature is the ability to copy any record. This is a good idea if you need to create a new record but want to base it on an existing one. 

Just go to the record header and click the `Copy` link. 

![Copy link for copying an existing record](wiki_images/advanced/copy-record.png)

Note that the metadata models still apply, so if you copy a record that is contained within another record, it will automatically be linked to the containing record. But you can still choose a different record if you want. 

## 4. Bulk uploading your data files

We have client tools available that can make the uploading of many or large files much easier than the browser method. This method is more involved in the sense that you need to download and install the tools once and set up your directory structure and file naming convention so that the tool can automatically relate the data files to the correct metadata records. But once it's set up you can submit your upload job for all of the files at once.

For more information, go to: [Bulk Upload with DERIVA Client Tools](/docs/bulk-upload-with-deriva-client-tools).



 
  
 