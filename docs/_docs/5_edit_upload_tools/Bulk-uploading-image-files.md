---
title: Bulk Uploading Image Files
permalink: /docs/bulk-uploading-image-files/
---

The easiest way to add imaging data is via the web interface, using the method described in [Submitting Specimen Data](../specimen-v3/). If you have many files to upload, however, it may be more convenient to use the DERIVA bulk uploader tool.

If you're not already familiar with the concepts and steps described in the [Submitting Specimen Data](../specimen-v3/) page, please review them. The bulk upload tool is a replacement for *6. Upload Image Files** from that page.

## Step 1: Create Specimen records
Create specimen records using either the the web interface, as described in [Submitting Specimen Data](../specimen-v3/), or the CSV process described in [Adding specimen records from a file](../adding-specimen-records-from-a-file/).

**Make sure you assign each record a unique Internal ID**; the Internal ID is used to link image files with the corresponding Specimen records.

## Step 2: Put images where the upload tool can find them
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

![Relationships between specimen Internal_ID values and image file names](https://raw.githubusercontent.com/wiki/informatics-isi-edu/gudmap-rbk/specimen-imgs/specimen-record-internal-id-tool.png)

### For 3D files:

* Create a folder called `deriva`.
* Within `deriva`, create a folder called `image_3d`
* Within `image_3d`, save your image files, using filenames with the following naming convention, where `image_type` is either `volume` or `surface`, depending on the type of data:

```
{internal_id}-{image-type}.{suffix}
```

Where:
* `{internal_id}` is exactly the same as the `Internal ID` value of the corresponding specimen.
* `{number}` is a number; if you have a specimen with multiple images, this will control the order in which they're displayed (if you only have one image per specimen, just use "1").
* `{suffix}` is the suffix, indicating the file type (`czi`, `jpeg`, `jpg`, `tif`, etc.)
* Note that a hyphen (`-`) is used to separate the `{internal_id}` and the `{image-type}` in the image filename.

## Step 3: Upload the files
Follow [these instructions](../bulk-upload-with-deriva-client-tools/) to upload your file, pointing the uploader at the `images` subfolder.

## Step 4: Fill in any missing data
Follow the instructions at [Submitting Specimen Data](../specimen-v3/) to add anatomical sites, antibodies, etc.

## Step 5: Update the curation status
Your new records will initially be marked "In Preparation" and will be visible only to consortium members. Change the Specimen records' status to "Submitted" to forward them on to the Biocurator for review and release.
