---
title: Bulk uploading image files
permalink: /docs/bulk-uploading-image-files/
---

The easiest way to add imaging data is via the web interface, using the method described in [Submitting Specimen Data](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Submitting-Specimen-Data). If you have many files to upload, however, it may be more convenient to use the Deriva bulk uploader tool.

If you're not already familiar with the concepts and steps described in the [Submitting Specimen Data](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Submitting-Specimen-Data) page, please review it and/or the tutorials linked there. The bulk upload tool is a replacement for Step 4 (Add Image Records) from that page.

## Step 1: Create Specimen records
Create specimen records using either the the web interface, as described in [Submitting Specimen Data](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Submitting-Specimen-Data), or the bulk upload process described in [Adding specimen records from a spreadsheet or CSV](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Adding-specimen-records-from-a-spreadsheet-or-CSV). Make sure you assign each record a unique Internal ID; the Internal ID is used to link image files with the corresponding Specimen records.

## Step 2: Create image files, and put them where the upload tool can find them.
In order for the upload tool to find your image files, you'll need to organize your files as follows:

### For 2D files:

* Create a folder called `deriva`.
* Within `deriva`, create a folder called `images`
* Within `images`, save your image files, using filenames with the following naming convention:

```
{internal_id}-{number}.{suffix}
```

Where:
* `{internal_id}` is the same as the `Internal_ID` value of the corresponding specimen
* `{number}` is a number; if you have a specimen with multiple images, this will control the order in which they're displayed (if you only have one image per specimen, just use "1").
* `{suffix}` is the suffix, indicating the file type (`czi`, `jpeg`, `tiff`, etc.)
* Note that a hyphen (`-`) is used to separate the `{internal_id}` and the `{number}` in the image filename.

For example:

![Relationships between specimen Internal_ID values and image file names](https://raw.githubusercontent.com/wiki/informatics-isi-edu/gudmap-rbk/specimen-imgs/uploader/spec_to_files.png)

### For 3D files:

* Create a folder called `deriva`.
* Within `deriva`, create a folder called `image_3d`
* Within `image_3d`, save your image files, using filenames with the following naming convention, where `image_type` is either `volume` or `surface`, depending on the type of data:

```
{internal_id}-{image-type}.{suffix}
```

Where:
* `{internal_id}` is the same as the `Internal_ID` value of the corresponding specimen
* `{number}` is a number; if you have a specimen with multiple images, this will control the order in which they're displayed (if you only have one image per specimen, just use "1").
* `{suffix}` is the suffix, indicating the file type (`czi`, `jpeg`, `tiff`, etc.)
* Note that a hyphen (`-`) is used to separate the `{internal_id}` and the `{image-type}` in the image filename.

## Step 3: Upload the files
Follow [these instructions](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Uploading-files-via-Deriva-client-tools) to upload your file, pointing the uploader at the `images` subfolder.

## Step 4: Fill in any missing data
Follow the instructions at [Submitting Specimen Data](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Submitting-Specimen-Data) to add anatomical sites, antibodies, etc.

## Step 5: Update the curation status
Your new records will initially be marked "In Preparation" and will be visible only to consortium members. Change the Specimen records' status to "Submitted" to forward them on to the biocurator for review and release.
