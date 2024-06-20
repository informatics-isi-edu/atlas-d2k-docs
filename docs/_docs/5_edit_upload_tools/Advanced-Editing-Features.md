---
title: Advanced Editing Features
permalink: /docs/advanced-editing-features/
---

The following are some very useful features of editing in the Data Browser that can make data entry much faster and easier. Note you must be logged in to take advantage of these features.

- [1. Clone](#1-clone)
- [2. Bulk Edit](#2-bulk-edit)
- [3. Copy](#3-copy)
- [4. Bulk uploading your data files](#4-bulk-uploading-your-data-files)


## 1. Clone

Whenever you are on any "Create" or "Edit" form, you can click the _Clone_ button in the upper right corner to create a duplicate of that form. You can keep clicking "Clone" to create another duplicate, or enter a number in the _Qty_ field and then click _Clone_.

![Screenshot of the multi-create buttons]({{ "/assets/wiki_images/advanced/multi-create-buttons.png" | relative_url }})


You can add many records at a time this way, but depending on the quality of your wireless connection, you might want to keep it to no more than 10 at a time.

What's especially helpful is that when you click either button, the new entries it generates **copies any field values from the last form appearing**. This means that you can fill out any common field values (ie, Species, Age Stage, etc) and they will be carried over as you Clone the records.

## 2. Bulk Edit

You can change and edit the values for the same field across multiple records at the same time.

To edit records in bulk:
1. Filter data to pull up a search for the records you want to change.
2. In the upper right corner above the search results, click _Bulk Edit_. All of the records in the search results will now be displayed in editing mode.
3. Find the field you want to change across all of the records and click the pencil icon to the left of the field.
4. Enter the new value and click `Apply`. You also have the option to `Clear All` or `Cancel` the operation.
5. Click the _Save_ button at the upper right corner of the page to save your changes.

Before you click _Save_, if you make a mistake, you can click the _Reset_ button and it will take you back to the initial state of the forms.

## 3. Copy

Another useful feature is the ability to copy any record. This is a good idea if you need to create a new record but want to base it on an existing one.

Just go to the record you would like to duplicate and click the _Copy_ button.

![Copy link for copying an existing record]({{ "/assets/wiki_images/advanced/copy-record.png" | relative_url }})


Note that the metadata models still apply, so if you copy a record that is contained within another record, it will automatically be linked to the containing record. But you can still choose a different record if you want.

## 4. Bulk uploading your data files

We have client tools available that can make the uploading of many or large files much easier than the browser method. This method is more involved in the sense that you need to download and install the tools once and set up your directory structure and file naming convention so that the tool can automatically relate the data files to the correct metadata records. But once it's set up you can submit your upload job for all of the files at once.

For more information, go to: [Bulk Upload with DERIVA Client Tools](/docs/bulk-upload-with-deriva-client-tools).
