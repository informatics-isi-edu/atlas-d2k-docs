---
title: Bulk Uploading Files with DERIVA Client Tools
permalink: /docs/uploading-files-using-deriva-client-tools/
---

NOTE: This page may be obsolete!

**On this page:**
- [Introduction](#introduction)
- [Preparing files for upload](#preparing-files-for-upload)
- [From a desktop system](#from-a-desktop-system)
  - [1. Initial setup](#1-initial-setup)
  - [2. Uploading files](#2-uploading-files)
  - [3. Logging out](#3-logging-out)
- [From a remote server](#from-a-remote-server)
  - [1. Initial setup](#1-initial-setup-1)
  - [2. Getting an authentication token](#2-getting-an-authentication-token)
  - [3. Uploading files](#3-uploading-files)
  - [4. Logging out](#4-logging-out)

## Introduction

The DERIVA Client tools allow you to authenticate with the system and upload files in bulk to the repository.

There are two versions of the client tool:
* [a graphical interface that can be run to upload files from your desktop system](#from-a-desktop-system), and
* [a command-line interface that can be used to upload files from a remote server](#from-a-remote-server)

Although the process for downloading and running the above tools are different, they both use the same directory structure designed for different data types.

## Preparing files for upload

Before you can use these tools, you'll need to set up your files using certain conventions so the tool can map the files to their appropriate records on our system.

* **For sequencing data**, please read [this section of Submitting Sequencing Data](../submitting-sequencing-data-v3#5-upload-sequencing-and-analysis-files).
* **For imaging data**, please read [Create a Specimen Record](../specimen-v2/#2-create-a-specimen-record).

## From a desktop system

### 1. Initial setup

1. **Download and install the DERIVA Client Tools:** Use the link [here](https://github.com/informatics-isi-edu/deriva-client#installer-packages-for-windows-and-macosx).

2. **Add a server configuration:** You only need to do this the first time you use the DERIVA Upload Utility from the Client Tools package.

  a. Launch the Deriva Upload Utility through the applications menu on Windows or MacOS.

  b. The tool will ask you if you want to add a server configuration. Click "yes" to bring up the "Options" screen (you can also do this at any time by clicking the "Options" button at the top of the page).

  c. Click `Add` to bring up the "Server Configuration" form and enter these values:

```
Host: www.atlas-d2k.org
Description: ATLAS-D2K
Catalog ID: 2
```

  d. Check the "Set as Default" and "Confirm configuration updates" fields, and click "OK".

  e. Then click "OK" again on the Options window.

![Server configuration window]({{ "/assets/wiki_images/submitting-data/sequencing_uploader/server-config.atlas.png" | relative_url }})

### 2. Uploading files

In the main Deriva-Upload window, click the "Login" button at the top to log in. This will pop up a login dialog window. Once you've logged in, you may see a window notifying you that an updated configuration is available and asking if you'd like to apply it; you should click "Yes" to update your configuration and dismiss the window.

Next, in the main Deriva-Upload window, click the "Browse" button and select the `deriva` directory you created above. You'll see all the files you created, listed as "Pending".

![Before upload]({{ "/assets/wiki_images/submitting-data/sequencing_uploader/pending.png" | relative_url }})

Click the "Upload" button to start the upload process. The status of each file will change as it's uploaded; for successful uploads, the status will change from "Pending" to "Complete".

### 3. Logging out

Authentication tokens expire after 30 minutes of activity; you can log out explicitly by clicking on the "Logout" button at the top of the window.


## From a remote server

Using the command-line interface on a remote server is a bit more complicated. First, you'll need to get an authentication token by running the DERIVA-Auth tool on your desktop. Then you'll run the command-line tool on the remote server.

### 1. Initial setup

On your desktop system, install the latest version of DERIVA-Auth [here](https://github.com/informatics-isi-edu/deriva-qt/releases) (for Mac or Windows desktops) or [here](https://github.com/informatics-isi-edu/deriva-qt) (for Linux desktops).

On the remote server, install the latest version of deriva-py:
```
pip3 install --upgrade git+https://github.com/informatics-isi-edu/deriva-py.git
```

### 2. Getting an authentication token

The uploader requires an authentication token to communicate with the server. Running the DERIVA-Auth tool on your desktop (through the applications menu on Windows or Mac, or with `deriva-auth` on Linux) will bring up an authentication window similar to the one used in the data browser. The first time you log in, you'll see a mostly-empty window:

![Initial DERIVA-Auth run]({{ "/assets/wiki_images/submitting-data/sequencing_uploader/deriva-auth-empty.png" | relative_url }})

In the "Server:" area, type in the name of the server (www.atlas-d2k.org) and click on `Add`. You should now see something that looks similar to the data browser login screen
![Login window]({{ "/assets/wiki_images/submitting-data/sequencing_uploader/deriva-auth-globus.png" | relative_url }})

Note: in subsequent runs, DERIVA-Auth might take you directly to this window (skipping the blank screen at the beginning). It's always a good idea to look at the hostname before you log in.

After logging in, you'll see an "Authentication Successful" message. Click the "Show Token" button; this will bring up another dialog box to verify that you really want to view the token (XXX - show-details.png). Click on "Show Details" to display the token.
!["Show Details" window]({{ "/assets/wiki_images/submitting-data/sequencing_uploader/show-details.png" | relative_url }})

### 3. Uploading files

On the server, run the command:

`deriva-upload-cli` --catalog 2 --token _token_ --catalog 2 _host_ _/path/to/_/deriva

where _token_ is the token cut-and-pasted from your DERIVA-Auth session, _host_ is `www.atlas-d2k.org`, and _/path/to/_/deriva is the path to the `deriva` directory you created above. For example:
```
deriva-upload-cli --catalog 2 --token xXXxxxxXXxxxxXxXXXxXxxxX www.atlas-d2k.org $HOME/deriva
```

### 4. Logging out

Authentication tokens expire after 30 minutes of activity; you can log out explicitly by clicking on the "Logout" button at the top of the DERIVA-Auth window.
