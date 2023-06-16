---
title: z Uploading Sequencing Data Files (obsolete)
permalink: /docs/z-uploading-sequencing-data-files-obsolete/
---

<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

	- [Prerequisites](#prerequisites)
	- [Creating database records (or gathering data from existing ones)](#creating-database-records-or-gathering-data-from-existing-ones)
	- [Preparing your files on disk](#preparing-your-files-on-disk)
		- [Preparing non-single-cell sequencing files](#preparing-non-single-cell-sequencing-files)
		- [Preparing single-cell RNASeq files](#preparing-single-cell-rnaseq-files)
		- [Supported file extensions](#supported-file-extensions)
	- [Downloading and running the client tool](#downloading-and-running-the-client-tool)
		- [From a desktop system](#from-a-desktop-system)
			- [Initial setup](#initial-setup)
			- [Uploading files](#uploading-files)
			- [Logging out](#logging-out)
		- [From a remote server](#from-a-remote-server)
			- [Initial setup](#initial-setup)
			- [Getting an authentication token](#getting-an-authentication-token)
			- [Uploading files](#uploading-files)
			- [Logging out](#logging-out)

<!-- /TOC -->

## Prerequisites
Before uploading a sequencing data file:
1. You'll need to download the appropriate client tool (more detail on that later on this page).
2. You must be a member of the `kidney-writers` group (if you've created records in the RBK or GUDMAP data browser, you're already in the group. If not, you can request membership [here](https://app.globus.org/groups/af0b4010-5b75-11e6-9575-22000aef184d/about)).
3. You should decide which data element in the data browser to attach the file to (you may want to review the [data model](https://docs.google.com/presentation/d/1Ee4seF4fgGMH5OuB_N6npaH_tGfUT7yFKKS64I9vbzE/edit#slide=id.g30b0a47b91_0_0) first):
* Single-cell data file are associated with Single Cell Metrics records.
* Other sequencing data files are associated with Replicate records.
* Files that pertain to multiple replicates or experiments (e.g., aggregate analysis results) are associated with Study records.

Once you've done that, you can create the database records, lay out your files on disk, and then run the uploader.

## Creating database records (or gathering data from existing ones)
Before you can upload your file, the Study, Single Cell Metrics, or Replicate record that you want to attach it to must already exist in the database. Detailed instructions for creating those records can be found [here](/docs/submitting-sequencing-data-v3)), but the parts that are pertinent to data file uploads are:
* In general, you'll create a Study first, then an Experiment (which will be associated with the Study), then a Replicate or Single Cell Metric (which will be associated with that Experiment). The only real requirement is that the records exist; you can attach files to records that someone else has created.
* A Study may have multiple Experiments associated with it. An Experiment may have multiple Replicate and/or Single Cell Metrics records associated with it. Each Study, Replicate, and Single Cell Metric may have multiple files associated with it.
* When creating a Study, you'll be asked to assign it an Internal ID. This should be a unique identifier that's meaningful to you. You'll need to know this identifier before you upload; we'll refer to it as the _study\_internal\_id_.
* When creating an Experiment, you'll be asked to assign it an Internal ID. This should be a unique identifier that's meaningful to you. You'll need to know this identifier before you upload; we'll refer to it as the _experiment\_internal\_id_.

## Supported file extensions

| Extension | File Type | Description (will appear in file caption) |
|---|---|---|
| R1.fastq.gz | FastQ | F reads |
| R2.fastq.gz | FastQ | R reads |
| bam | bam | alignment |
| bed | bed | positive regions |
| bw | bigWig | visualization track |
| rpkm.txt | txt | expression value |
| tpm.txt | txt | expression value |

## Preparing your files on disk
The upload tools will use the names of files and directories (folders) to determine what kind of files you're uploading and which data records to attach them to. We support the following preparation procedures:  
* [Mass sequencing (e.g. mRNA-Seq, ATAC-Seq, CHIP-Seq)](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Uploading-Sequencing-Data-Files/_edit#preparing-mass-sequencing-eg-non-single-cell-files)
* [Single-cell RNA](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/Uploading-Sequencing-Data-Files/_edit#preparing-single-cell-rnaseq-files)

### Preparing mass sequencing (e.g. non single-cell) files

The layout of folders for mass sequencing files is:
```
$userid
  \- deriva
    \- Seq
      \- <Experiment Internal ID> 
        \- <Biological Replicate Number>_<Technical Replicate Number>_<Custom Text>.R1.fastq.gz
        \- <Biological Replicate Number>_<Technical Replicate Number>_<Custom Text>.R2.fastq.gz
        \- <Biological Replicate Number>_<Technical Replicate Number>_<Custom Text>.bam
        \- <Biological Replicate Number>_<Technical Replicate Number>_<Custom Text>.bed
        \- <Biological Replicate Number>_<Technical Replicate Number>_<Custom Text>.bw
        \- <Biological Replicate Number>_<Technical Replicate Number>_<Custom Text>.txt
          or 
        \- <Replicate RID>_<Custom Text>.R1.fastq.gz
        \- <Replicate RID>_<Custom Text>.R2.fastq.gz
        \- <Replicate RID>_<Custom Text>.bam
        \- <Replicate_RID>_<Custom Text>.bed
        \- <Replicate_RID>_<Custom Text>.bw
        \- <Replicate RID>_<Custom Text>.txt
```
where
  - `deriva` is the name of our software 
  - `Seq` is a subfolder of `deriva`. This indicates that everything within is the mass sequencing data (e.g. non single-cell)
  - `<Study Internal ID>` is what is specified in the study metadata e.g. `NPC_stability`
  - `<Experiment Internal ID>` is what is specified in the sample metadata e.g. `mNPC_RNA`
  - `<Biological Replicate Number>` is the biological replicate number associated with the replicate e.g. `1`
  - `<Technical Replicate Number>` is the technical replicate number associated with the replicate e.g. `1`
  - `<Replicate RID>` is the replicate RID e.g. `Q-Y500`
  - `<Custom Text>` is other metadata associated with the file e.g. `sorted`
  - `<File Extension>` is one of the file extensions that we current supported. _File Extension_ tells the system what type of file is being uploaded.

**Examples:**

If you have a study called "NPC_stability" with experiments "mNPC_RNA" and "mNPC_ATAC", you'd create two folders `deriva/Seq/NPC_stability/mNPC_RNA` and `deriva/Seq/NPC_stability/mNPC_ATAC` (on Windows, the paths would be `deriva\Seq\NPC_stability\mNPC_RNA` and `deriva\Seq\NPC_stability\mNPC_ATAC`). All the sequencing files are then placed into the respective experiment folders. In the example below, we use _Biological Replicate Number_ and _Technical Replicate Number_ to name the files in experiment "mNPC_RNA" and use the Replicate _RID_ to name the files in the experiment "mNPC_ATAC". Both file naming conventions will be accepted by the client tool. See actual examples of metadata and files in [the NPC_stability Study](https://www.gudmap.org/chaise/record/#2/RNASeq:Study/RID=Q-Y4GW). 

```
$userid
  \- deriva
    \- Seq
      \- NPC_stability  
        \- mNPC_RNA 
          \- 1_1.R1.fastq.gz
          \- 1_1.R2.fastq.gz
          \- 1_1_sorted.bed
          \- 1_1_normalized_profile.bw
          \- 1_1.kpm.txt
          \- ...
        \- mNPC_ATAC
          \- Q-Y5CC.R1.fastq.gz
          \- Q-Y5CC.R2.fastq.gz
          \- Q-Y5CC_sorted.bed
          \- Q-Y5CC_normalized_profile.bw
          \- Q-Y5CC.kpm.txt
          \- ...
```

### Preparing single-cell RNASeq files

The layout of folders for mass sequencing files is:
```
$userid
  \- deriva
    \- scRNASeq
      \- <Experiment Internal ID> 
        \- <Biological Replicate Number>_<Technical Replicate Number>_<Custom Text>.R1.fastq.gz
        \- <Biological Replicate Number>_<Technical Replicate Number>_<Custom Text>.R2.fastq.gz
        \- <Biological Replicate Number>_<Technical Replicate Number>_<Custom Text>.bam
        \- <Biological Replicate Number>_<Technical Replicate Number>_<Custom Text>.bed
        \- <Biological Replicate Number>_<Technical Replicate Number>_<Custom Text>.bw
        \- <Biological Replicate Number>_<Technical Replicate Number>_<Custom Text>.txt
          or 
        \- <Single Cell Metrics RID>_<Custom Text>.R1.fastq.gz
        \- <Single Cell Metrics RID>_<Custom Text>.R2.fastq.gz
        \- <Single Cell Metrics RID>_<Custom Text>.bam
        \- <Single Cell Metrics RID>_<Custom Text>.bed
        \- <Single Cell Metrics RID>_<Custom Text>.bw
        \- <Single Cell Metrics RID>_<Custom Text>.txt
```
where
  - `deriva` is the name of our software 
  - `Seq` is a subfolder of `deriva`. This indicates that everything within is the mass sequencing data (e.g. non single-cell)
  - `<Study Internal ID>` is what is specified in the study metadata e.g. `mouse_SC_RNASeq`
  - `<Experiment Internal ID>` is what is specified in the sample metadata e.g. `m1_e11_cortex`, `m2_p0_cortex`
  - `<Biological Replicate Number>` is the biological replicate number associated with the replicate e.g. `1`
  - `<Technical Replicate Number>` is the technical replicate number associated with the replicate e.g. `1`
  - `<Single Cell Metrics RID>` is the Single Cell Metrics RID e.g. `Q-Y4C4`, `Q-Y4HM`
  - `<Custom Text>` is other metadata associated with the file e.g. `sorted`
  - `<File Extension>` is one of the file extensions that we current supported. _File Extension_ tells the system what type of file is being uploaded.

**Examples:**
If you have a single-cell RNA study called "mouse_SC_RNASeq" with experiments "m1_e11_cortex" and "m2_p0_cortex", you'd create two folders `deriva/scRNASeq/mouse_SC_RNASeq/m1_e11_cortex` and `deriva/scRNASeq/m2_p0_cortex` (on Windows, the paths would be `deriva\scRNASeq\mouse_SC_RNASeq\m1_e11_cortex` and `deriva\scRNASeq\m2_p0_cortex`). All the sequencing files are then placed into the respective experiment folders. In the example below, we use _Biological Replicate Number_ and _Technical Replicate Number_ to name the files in experiment "m1_e11_cortex" and use the Single Cell Metrics _RID_ to name the files in the experiment "m2_p0_cortex". Both file naming conventions will be accepted by the client tool. See actual examples of metadata and files in [the mouse_SC_RNASeq Study](https://www.gudmap.org/chaise/record/#2/RNASeq:Study/RID=Q-Y4GT). 

```
$userid
  \- deriva
    \- scRNASeq
      \- mouse_SC_RNASeq  
        \- m1_e11_cortex 
          \- 1_1.R1.fastq.gz
          \- 1_1.R2.fastq.gz
          \- 1_1_sorted.bed
          \- 1_1_normalized_profile.bw
          \- 1_1.kpm.txt
          \- ...
        \- m2_p0_cortex
          \- Q-Y4HM.R1.fastq.gz
          \- Q-Y4HM.R2.fastq.gz
          \- Q-Y4HM_sorted.bed
          \- Q-Y4HM_normalized_profile.bw
          \- Q-Y4HM.kpm.txt
          \- ...
```


## Downloading and running the client tool

There are two versions of the client tool: a graphical interface that can be run to upload files from your desktop system, and a command-line interface that can be used to upload files from a remote server. Both use the same directory structure described above, but the process for downloading and running the tools are different.

### From a desktop system

#### Initial setup

First download and install the latest version of DERIVA-Upload [here](https://github.com/informatics-isi-edu/deriva-qt/releases) (for Mac or Windows desktops) or [here](https://github.com/informatics-isi-edu/deriva-qt) (for Linux desktops).

The first time you launch deriva-upload (through the applications menu on Windows or MacOS, or with the `deriva-upload` command on Linux), the tool will ask you if you want to add a server configuration. Click "yes" to bring up the "Options" screen (you can also do this at any time by clicking the "Options" button at the top of the page).

![Initial server configuration window](/assets/wiki_images/submitting-data/sequencing_uploader/server-config.blank.png)

Click `Add` to bring up the "Server Configuration" form and enter these values:
Host: www.gudmap.org (or www.rebuildingakidney.org)
Description: GUDMAP (or RBK)
Catalog ID: 2
check the "Set as Default" and "Confirm configuration updates" buttons, and click "OK"

![Server configuration window](/assets/wiki_images/submitting-data/sequencing_uploader/server-config.gudmap.png)

#### Uploading files

In the main Deriva-Upload window, click the "Login" button at the top to log in. This will pop up a login dialog window. Once you've logged in, you may see a window notifying you that an updated configuration is available and asking if you'd like to apply it; you should click "Yes" to update your configuration and dismiss the window.

![Configuration update window](/assets/wiki_images/submitting-data/sequencing_uploader/update-config.gudmap.png)


Next, in the main Deriva-Upload window, click the "Browse" button and select the `deriva` directory you created above. You'll see all the files you created, listed as "Pending".
![Before upload](/assets/wiki_images/submitting-data/sequencing_uploader/pending.png)

Click the "Upload" button to start the upload process. The status of each file will change as it's uploaded; for successful uploads, the status will change from "Pending" to "Complete".

#### Logging out

Authentication tokens expire after 30 minutes of activity; you can log out explicitly by clicking on the "Logout" button at the top of the window.

### From a remote server

Using the command-line interface on a remote server is a bit more complicated. First, you'll need to get an authentication token by running the DERIVA-Auth tool on your desktop. Then you'll run the command-line tool on the remote server.

#### Initial setup

On your desktop system, install the latest version of DERIVA-Auth [here](https://github.com/informatics-isi-edu/deriva-qt/releases) (for Mac or Windows desktops) or [here](https://github.com/informatics-isi-edu/deriva-qt) (for Linux desktops).

On the remote server, install the latest version of deriva-py:
```
pip3 install --upgrade git+https://github.com/informatics-isi-edu/deriva-py.git
```

#### Getting an authentication token

The uploader requires an authentication token to communicate with the server. Running the DERIVA-Auth tool on your desktop (through the applications menu on Windows or Mac, or with `deriva-auth` on Linux) will bring up an authentication window similar to the one used in the data browser. The first time you log in, you'll see a mostly-empty window:
![Initial DERIVA-Auth run](/assets/wiki_images/submitting-data/sequencing_uploader/deriva-auth-empty.png)

In the "Server:" area, type in the name of the server (www.gudmap.org or www.rebuildingakidney.org) and click on `Add`. You should now see something that looks similar to the data browser login screen
![Login window](/assets/wiki_images/submitting-data/sequencing_uploader/deriva-auth-globus.png)

Note: in subsequent runs, DERIVA-Auth might take you directly to this window (skipping the blank screen at the beginning). It's always a good idea to look at the hostname before you log in.

After logging in, you'll see an "Authentication Successful" message. Click the "Show Token" button; this will bring up another dialog box to verify that you really want to view the token (XXX - show-details.png). Click on "Show Details" to display the token.
!["Show Details" window](/assets/wiki_images/submitting-data/sequencing_uploader/show-details.png)

#### Uploading files

On the server, run the command:

`deriva-upload-cli` --catalog 2 --token _token_ --catalog 2 _host_ _/path/to/_/deriva

where _token_ is the token cut-and-pasted from your DERIVA-Auth session, _host_ is `www.gudmap.org` or `www.rebuildingakidney.org`, and _/path/to/_/deriva is the path to the `deriva` directory you created above. For example:
```
deriva-upload-cli --catalog 2 --token xXXxxxxXXxxxxXxXXXxXxxxX www.gudmap.org $HOME/deriva
```

#### Logging out

Authentication tokens expire after 30 minutes of activity; you can log out explicitly by clicking on the "Logout" button at the top of the DERIVA-Auth window.









