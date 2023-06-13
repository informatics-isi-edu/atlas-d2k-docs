---
title: Submitting Single Cell Visualization Files
permalink: /docs/single-cell-visualization-files/
---

**DRAFT**

## Gene Naming Convention 
Please use numeric NCBI Gene ID when naming your files and metadata. The [Gene Page](https://www.gudmap.org/chaise/recordset/#2/Common:Gene) lists the genes records existing in the Consortium repository.

## Process
1. Create the [Visualization Application](https://www.gudmap.org/chaise/recordedit/#2/RNASeq:Visualization_Application) record.
* In the Create menu, choose "Sequencing Data" and then "Visualization Application". Enter a name, description, and maintainer (e.g., your name or contact email - we will probably expand on this section in the future).
* Once that has been created, add one or more "Application File Tag" records to it (by clicking `Add` under "Application File Tag"). These tags will later be associated with files that you (or other data providers) upload; they can be [queried by applications ](https://github.com/informatics-isi-edu/rbk-project/wiki/Proposed-process-for-creating-new-RNASeq-visualization-apps) and will be used by our software to determine the order in which the files are displayed. If your application provides image files for our server to display, the tags should probably be things like "T-SNE" or "UMAP".

2. Create Cluster records. Go to your Study, click `Add` on top of the "Study Cluster" section, and enter a name and (optionally) a number and description for each cluster.

3. Create Visualization records. An automated process for this is currently in development.

4. Create a CSV file indicating gene/cluster relationships, with lines of the form
```
study_internal_id,cluster_name,ncbi_geneid
```

5. Create files according to this Directory Structure (described below).

## Directory Structure
```
$userid
  \- deriva
    \- Seq
      \- <Study Internal ID>                       # E.g., my_study_1
        \- application_files      
          \- <Application Name>                    # The application name corresponding to an   
                                                   #   Visualization_Application record in the repository.
            \- <Application File Tag>              # The application file tag (e.g., T-SNE, Violin) corresponding 
                                                   #   to an Application_File_Tag record in the repository.
              \- <Study-wide File>                 # Files that are not specific to a cluster or gene (e.g. all_tsne.png)
              \- ...
              \- genes                             # The word "genes", indicating that files  
                                                   #   in this directory are gene-specific
                \- <NCBI Gene ID>_<Display Rank>.<Suffix>  # e.g. 10736_1.png  
                \- ...
              \- <Cluster_Name>                    # Cluster-specific folder (e.g., "Epithelial Cells"). The folder name
                                                   #   corresponds to in the Study_Cluster record in the repository.
                \- genes                           # The word "genes", indicating that the files in this directory
                                                   #    are gene-specific
                  \- <NCBI Gene ID>_<Display Rank>.<suffix>
                  \- ...
```                 
* deriva
  * Seq
    * `<Study Internal ID>`
      * application_files
        * `<Application Name>` 
          * `<Application File Tag>`
            * `<Study-wide File>`     **--_study-wide files_**
            * ...
            * `<Study-wide File>`
            * genes   
              * `<NCBI Gene ID>_<Display Rank>.<Suffix>`   **--_gene specific files_**
              * ...
              * `<NCBI Gene ID>_<Display Rank>.<Suffix>`
            * `<Cluster Group Name>`
              * `<Cluster Group Specific File>`   **--_cluster-group specific files_**
              * ...
              * `<Cluster Group Specific File>`
              * genes 
                * `<NCBI Gene ID>_<Display Rank>.<Suffix>`  **--_cluster-group and gene specific files_**
                * ... 
                * `<NCBI Gene ID>_<Display Rank>.<Suffix>`  




where
* `deriva` is the top-level directory. Deriva is the name of our software.
* `Seq` indicates that the folder contains sequencing data
* `<Study Internal ID>` is the `Internal_ID` field of an existing `Study` record.
* `application_files` indicates that the folder contains application files
* `<Application Name>` is the name of a visualization application (e.g. K.I.T.) registered in our server. Click [Visualization Application](https://www.gudmap.org/chaise/recordset/#2/RNASeq:Visualization_Application) to check for the existing applications. There are 4 different types of files and sub-directory structure that go under this folder: 
  1. **study-wide files**: The file path is `<Application File Tag> / <file>`
  2. **gene-specific files**: The file path is `<Application File Tag> / genes / <NCBI_ID>_<rank>.png` where "gene" is the exact word.
  3. **cluster-group specific files**: include files that are specific to a cluster group but not a gene. The file path is `<Application File Tag> / <Cluster Group Name> / <file>.png`
  4. **cluster-group and gene specific files**: includes files that are specific to both a cluster group and a gene. The path is 
`<Application Name> / <File Tag> / <Cluster Group> / genes / <NCBI_ID>_<rank>.png`  where "genes" is the exact word.  
* `<Application File Tag>` is the name of a tag (e.g. Feature, T-SNE, UMAP, Violin) associated with files produced by the above application. Click [Application File Tag](https://www.gudmap.org/chaise/recordset/#2/RNASeq:Application_File_Tag) to check for the existing application file tags. 
There are 4 different types of files  and therefore different paths of directory structures that go under this folder:  
* `<Study-wide File>` corresponds to image or analysis files that are not specific to clusters or genes. 
* `genes` indicates that the folder contains gene-specific files
* `Cluster Name` (e.g. Cluster_1) indicates the cluster number. All the folders/files under this cluster folder are specific to this cluster
* `<NCBI Gene ID>_<Display Rank>.<Suffix>` (e.g. 10736_1.png) represents gene-specific files. 
  * `<NCBI Gene ID>` is the NCBI Gene ID. This ID uniquely identifies the specific gene in the repository.
  * `<Display Rank>` if exists represents the preferred display rank of files associated with the gene. For example, if T-SNE should be displayed before Violin, then all the files under T-SNE folder should have `<Display Rank>` of 1 and all the files under Violin should have `<Display Rank>` of 2. This display rank can be queried by applications and will be used by our software to determine the order in which the files are displayed.
  * `<Suffix>` (e.g. png, jpg, txt) is the file extension.  


**Examples:**
```
$userid
  \- deriva
    \- Seq
      \- my_study_1
        \- application_files      
          \- K.I.T.        # directory structure from KIT
            \- T-SNE
              \- genes            # contains per gene images
                \- 59_1.png       # gene ACTA2, displayed with rank 1
                \- 800_1.png      # gene CALD1, displayed with rank 1
                \- ...
            \- Violin
              \- genes            # contains per gene images
                \- 59_2.png       # gene ACTA2, displayed with rank 2
                \- 800_2.png      # gene CALD1, displayed with rank 2
                \- ...
            \- Dotplot
              \- genes            # contains per gene images
                \- 59_3.png       # gene ACTA2, displayed with rank 3
                \- 800_3.png      # gene CALD1, displayed with rank 3
                \- ...
          \- Strand_Viz            # directory structure from Strand Viz
            \- T-SNE
              \- All
                \- genes            # contains per gene images
                  \- <Gene NCBI ID>_<Display Rank>.png 
                  \- ...
              \- Epithelial Cells
                \- genes            # contains per gene images
                  \- <Gene NCBI ID>_<Display Rank>.png 
                  \- ...
            \- Violin
              \- All
                \- genes            # contains per gene images
                  \- <Gene NCBI ID>_<Display Rank>.png 
                  \- ...
              \- Epithelial Cells
                \- genes            # contains per gene images
                  \- <Gene NCBI ID>_<Display Rank>.png 
                  \- ...
 
```

