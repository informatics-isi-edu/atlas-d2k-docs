---
title: Standard file formats for data submission
permalink: /docs/standard-files-and-formats-for-submission/
---

On this page, you'll find the standard files and formats agreed upon by the GUDMAP and RBK Consortium for data submissions:

Table of contents:
- [General file format requirements](#general-file-format-requirements)
  - [Sequencing formats](#sequencing-formats)
  - [High resolution image formats](#high-resolution-image-formats)
  - [Thumbnail formats](#thumbnail-formats)
  - [Video formats](#video-formats)
- [Mandatory assets for data submission (detailed)](#mandatory-assets-for-data-submission-detailed)
  - [Sequencing data](#sequencing-data)
  - [H\&E data](#he-data)
  - [IHC/Immunofluorescence data](#ihcimmunofluorescence-data)
  - [In-situ Hybridization (ISH) Specimen](#in-situ-hybridization-ish-specimen)
  - [Antibodies](#antibodies)
  - [Protocols](#protocols)


## General file format requirements

### Sequencing formats

* .fastq
* .bam


### High resolution image formats 

These are in order of desirability (providing the best user experience):

* Native file formats: CZI, LIF, LSM, VSI, Panaroma

* OME-TIF, TIFF

* JPG, PNG, GIF


### Thumbnail formats

* **General:** The thumbnail should highlight the area of interest in your original image. It is usually displayed on the general search page to provide quick impression of the original images.
* **Resolution:** Make the height and width of the thumbnail 150 pixels and around 72 DPI.
* **File format**: .png, .jpeg (Note: These are browser-supported image formats)

### Video formats

* .mp4
* .avi

## Mandatory assets for data submission (detailed)

### Sequencing data

For RNA-Seq, CHIP-Seq, ATAC-Seq and scRNA-seq data:

<table>
  <tr>
    <th>File Type</th>
    <th>File Format</th>
    <th>Mandatory?</th>
  </tr>
  <tr>
    <td>Sequencing files</td>
    <td>F/R read fastq (.fastq.gz)</td>
    <td>Mandatory</td>
  </tr>
  <tr>
    <td>Alignment </td>
    <td>BAM (.bam)</td>
    <td>Mandatory</td>
  </tr>
  <tr>
    <td>Positive Region</td>
    <td>BED (.bed)</td>
    <td>If available</td>
  </tr>
  <tr>
    <td>Visualization track</td>
    <td>BigWig (.bw)</td>
    <td>If available</td>
  </tr>
  <tr>
    <td>Expression value (RPKM/TPM)</td>
    <td>Text (.txt)</td>
    <td>If available</td>
  </tr>
  <tr>
    <td>Single-cell Analysis file</td>
    <td>.csv</td>
    <td>If available</td>
  </tr>
</table>


### H&E data

<table>
  <tr>
    <th>File Type</th>
    <th>File Format</th>
    <th>Mandatory?</th>
  </tr>
  <tr>
    <td>H&E images</td>
    <td>[High resolution image formats (from devices)](#high-resolution-image-formats)</td>
    <td>Mandatory</td>
  </tr>
  <tr>
    <td>H&E thumbnails</td>
    <td>.jpeg or .png for preview</td>
    <td>If available</td>
  </tr>
</table>


### IHC/Immunofluorescence data

<table>
  <tr>
    <th>File Type</th>
    <th>File Format</th>
    <th>Mandatory?</th>
  </tr>
  <tr>
    <td>Immunofluorescence images </td>
    <td>[High resolution image formats (from devices)](#high-resolution-image-formats)</td>
    <td>Mandatory</td>
  </tr>
  <tr>
    <td>Immunofluorescence videos</td>
    <td>.mp4, .avi</td>
    <td>If available</td>
  </tr>
  <tr>
    <td>Immunofluorescence thumbnails</td>
    <td>.jpeg or .png for preview</td>
    <td>If available</td>
  </tr>
</table>


### In-situ Hybridization (ISH) Specimen

<table>
  <tr>
    <th>File Type</th>
    <th>File Format</th>
    <th>Mandatory?</th>
  </tr>
  <tr>
    <td>Images</td>
    <td>[Output from device](#high-resolution-image-formats) **(Do not downsample)**</td>
    <td>Mandatory</td>
  </tr>
  <tr>
    <td>Thumbnails</td>
    <td>.jpeg or .png for preview</td>
    <td>If available</td>
  </tr>
</table>


### Antibodies

<table>
  <tr>
    <th>File Type</th>
    <th>File Format</th>
    <th>Mandatory?</th>
  </tr>
  <tr>
    <td>Antibody test summary sheets</td>
    <td>.jpeg, .png, .pdf</td>
    <td>Mandatory</td>
  </tr>
  <tr>
    <td>Antibody test images</td>
    <td>.jpeg, .png</td>
    <td>Mandatory</td>
  </tr>
</table>


### Protocols

<table>
  <tr>
    <th>File Type</th>
    <th>Preferred File Format</th>
    <th>Mandatory?</th>
  </tr>
  <tr>
    <td>Source publication/manuscript</td>
    <td>.pdf</td>
    <td>If available</td>
  </tr>
  <tr>
    <td>Figure images</td>
    <td>.jpg, .png</td>
    <td>If available</td>
  </tr>
  <tr>
    <td>Figure videos</td>
    <td>.mp4, .avi</td>
    <td>If available</td>
  </tr>
</table>


