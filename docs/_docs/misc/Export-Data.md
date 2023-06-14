---
title: Export Data
permalink: /docs/export-data/
---


## 1. Obtain the exported BDBAG. 

The BDBAG export is available on the detail page of the data of your interest on [www.gudmap.org](https://www.gudmap.org) and  [www.rebuildingakidney.org](https://www.rebuildingakidney.org). For example, navigate to the record of interest e.g. https://www.gudmap.org/chaise/record/#2/RNASeq:Study/RID=16-DW82, 
then click the "Export" link towards the upper right part of the screen and choose BAG.

<img src="https://github.com/informatics-isi-edu/gudmap-rbk/blob/master/wiki_images/export_data/export_bdbag.PNG" alt="export bdbag" width="600"/>


A progress window appears saying that the BAG is being created.

<img src="https://github.com/informatics-isi-edu/gudmap-rbk/blob/master/wiki_images/export_data/export_progress_bar.PNG" alt="export progress" width="600" />


Then a ZIP file is downloaded to your current directory with the metadata files describing the data (including appropriate MD5 checksums). e.g. Study_16-DW82.zip


If you unzip the file, you will see a list of dbbag manifest files and folders. The "data" folder contains the exported metadata in the csv format relevant to the dataset of your interest e.g. Study.csv, Experiment.csv, etc. 
The actual asset files are listed in the BDBAG manifest and can be downloaded using bdbag commands showing the next step.

<img src="https://github.com/informatics-isi-edu/gudmap-rbk/blob/master/wiki_images/export_data/export_unzipped.PNG" alt="export file unzipped" width="800"/>

 
## 2. Download and install DERIVA Client Tools on the local computer.
The DERIVA Client Tools ([deriva-client](https://github.com/informatics-isi-edu/deriva-client)) are a set of software packages that allow users to interact with DERIVA platform servers.

* Windows and Mac users, please download and install bundle [here](https://github.com/informatics-isi-edu/deriva-client-bundle/releases)


* Linux users, please install deriva-client. A Python 3.5.4 or greater system installation is required. The latest stable version of Python is recommended. 
Please refer to [install instruction](https://github.com/informatics-isi-edu/deriva-client#deriva-client).

The following two programs are necessary to fetch the exported BDBAG files.  
* deriva-auth: used for logging in to update credential.
* bdbag: used for downloading files.


Users could open the command line and run following to see if bdbag installed correctly or not.
```
bdbag --version
```
if not installed, run following command
```
pip install bdbag
```
## 3. Login using DERIVA Authentication Agent
Open DERIVA Authentication Agent to log in. Run following command in command line or click the "DERIVA Authentication Agent" on Desktop.
```
deriva-auth
```

Type in the server name i.e. www.gudmap.org or www.rebuildingakidney.org to login using different types of accounts through Globus.

<img src="https://github.com/informatics-isi-edu/gudmap-rbk/blob/master/wiki_images/export_data/login_deriva_auth.PNG" alt="deriva login page" width="800"/>


After login successfully.


<img src="https://github.com/informatics-isi-edu/gudmap-rbk/blob/master/wiki_images/export_data/login_deriva_success.PNG" alt="deriva login success" width="800"/>


## 4. Export source files using bdbag
### 4.1 Download source files on the local computer

Open the command line window and run following commands:

To materialize the bag (e.g. download all the files listed in "fetch.txt")

```
bdbag --materialize  "download\path\Study_16-DW82.zip" 
```

User could also download all the files with a particular file extensions (e.g. fastq.gz).
```
bdbag --resolve-fetch all --fetch-filter filename$*fastq.gz "download\path\Study_16-DW82"
```

User could also download only the missing with a particular file extensions (e.g. fastq.gz).
```
bdbag --resolve-fetch missing --fetch-filter filename$*fastq.gz "download\path\Study_16-DW82"
```

User could also filter and only download files of limited size.
```
bdbag --resolve-fetch all --fetch-filter "length<=623874671" "download\path\Study_16-DW82" 
```

for this example, the downloaded files will show up in folder "./data/asset/"


Here is the detailed instruction on how to use the bdbag command: https://github.com/fair-research/bdbag/blob/master/doc/cli.md#bdbag-command-line-interface-cli

### 4.2 Download source files on the cluster/server
1. Install bdbag on the server
```
pip install bdbag
```
2. Make sure you have logged in using DERIVA Authentication Agent on your local computer.
3. Copy "deriva-cookies.txt" from local to the server under the folder "/home/username/.bdbag"
4. Copy the downloaded and unzipped folder(e.g.Study_16-DW82) to the server
5. Open the command line on the server and Run bdbag commands showing in section 4.1

