---
title: GUDMAP Requirements Sessions
permalink: /docs/gudmap-requirements-sessions/
---

This page will compile summaries of requirements/feedback from each group in July 2017.
- [Questions](#questions)
- [Data Submission Plans](#data-submission-plans)
- [Sessions](#sessions)
  - [Southard-Smith](#southard-smith)
  - [Vezina](#vezina)
  - [Tissue Hub](#tissue-hub)
  - [Keast](#keast)
  - [Li](#li)
  - [McMahon](#mcmahon)
  - [Mendelsohn](#mendelsohn)
  - [Cohn](#cohn)

# Questions

- Introduction: 
  - We would like to focus on the data and functionality that you find useful to your research and  community. Please don't worry about whether its achievable. We will gather all the suggestions, evaluate the potential solutions and prioritize the work later.
  - We are working on the new GUDMAP site that has a soft launch in November 2017, and is targeted to release in April 2018. 
- Questions about data: 
  - What kinds of information do you need for your research?
  - What kinds of searches do you perform on genitourinary data?
  - What kinds of searches would you like to perform that you may not be able to? 
  - What are your data submission plans for the next six months?
- Old GUDMAP site
  - How often do you or your lab members use the old GUDMAP site? Every week, a few times a month, etc. 
  - What do you usually use the site for? 
  - What features do you like most about the current site? 
  - What features do you wish to have improved?  
- New GUDMAP site (if time permits)
  - Are you familiar with the new site? Have you used the site? 
  - Get general feedback on the static site
  - Get feedback on the gene data. 
    - What's missing on the main gene page. 
    - What's missing on the individual gene detailed page. 
    - Heatmap 
  - If user plans to submit RNASeq data, introduce them to the RNASeq sample page containing metadata. 

# Data Submission Plans

**Southard-Smith**
* Images of fetal and postnatal LUT that express various transgene reporters and have been stained by immunohistochemistry
* single cell RNA-Seq using dropSeq. Seurat for analysis.

**Vezina**
* Currently finishing up paper in next 2 weeks and will send around for review.
* High resolution immunohistochemical stains for mouse (not wildtype, cre-mediated allele) - some large (1cm in width) made with Leica confocal
* How would you like those displayed? Maximum intensity projection, click on and off different layers (4 diff channels associated). Would like simple annotation layer. Just example cells. Chad would do the annotation.
* To do that, need to submit raw files, OMI TIFs, maximum intensity projections, representational layers and then add the annotations.
* Intend to submit human images, but still waiting on the right specimens, so may not happen in next 6 months.

**Keast**
* Still finishing GUDMAP2. Edinburgh has RNA-Seq. Waiting to send any further data to new Hub. 
* Will be images of neurons and ganglia with description and numerical data. 
* Excited that new Hub would be able to visualize the numerical data (histogram/plots)

**Li**
* already have images and video to submit now.
* Videos: morphological transformations over developmental changes. Region of anatomy over time.
* Images: 3-D
* May be good for Education site
* May have transcriptome data (rna-seq)
* Some of the data may need to be embargoed.

**McMahon**
* 75 TIF stacks - confocal images, AMIRA segmented subjects. 
* Large number mirror - 350 NIFTI 
* 30 AVI movie files - linked to TIF/AMIRA objects 
* 5 Excel files

**Mendelsohn**
* Immunohistochemical - 3 or 4 channels 
* 50 images in-situ 
* 10-20 single-cell RNA-Seq and RNA-Seq mouse

**Cohn**
* RNA-Seq
* histological data - sending slides to USC scanner and from there to the Hub (just like Andy's data)
* microCT data

# Sessions
## Southard-Smith

Tend to look for:
- expression patterns
- in situ 
- labeling of genes/finding gene of interest

On the old GUDMAP site, tended to search on gene names or, since working with Janet Keast, search by her group.

Would like:
- Perform Boolean searches
- Show results for different genes (for example) show up on the same page. Now, have to pull up search results in different browser tabs and go back and forth.
- Matrix of heatmaps (like GXD database: http://www.informatics.jax.org/expression.shtml )
- Break out by age stage
- Does NOT like Theiler stage - can we use embryonic days? Or map between

Comments on old site:
- Not intuitive, could use prompts "would you like to see x? go here" something like that.
- Do like the submission tool - lots of dropdown boxes I can just choose the right values.

Data submission plans for the next six months:
- Images of fetal and postnatal LUT that express various transgene reporters and have been stained by immunohistochemistry
- single cell RNA-Seq using dropSeq. Seurat for analysis.

Comments on new site:
- Tutorials 
  - have wrong attributions (Michelle will bring up on next monthly call)
  - should have more descriptive title (Development Tutorial...)
  - Instead of TOC, would be better to use anatomical issues that you click to drill down to different areas (like Allan Brain Atlas, http://www.brain-map.org/ )
- Homepage: image takes up too much real estate
- Would like a demo of new submission tool (Hub is planning on doing that about month before it rolls out in Nov).


## Vezina

Chad is different than most other gudmap projects. Focus on prostate _development_ rather than disease, which is of interest to only 5 or 6 other scientists in the world. Most prostate researchers shut down at the mention of the word "development". But Chad argues that understanding the mechanisms of growth which contribute to those diseases is important.

No much prostate development data out there, pretty much just what my lab is producing. But does look for RNA expression data on GENEPaint. Takes it with a grain of salt - timepoints are irrelevant.

Looking for pathways and androgen receptors

Would like to search for specific cell types, compare time points, would also like to see differences in gene expression across sex.

Side note: Chad works with antibodies in the OBrien Center and could ingest some for RBK site. (see PDF below)
http://www.urology.wisc.edu/system/assets/1232/List_of_validated_antibodies.pdf?1467059431 

How would you like to search?
- Forward direction - start with anatomical pictures - ie, click on image of prostate (which could be low-rez) and see higher rez more detailed image of cell types (ie luminal epithelial cells) and then see what are mRNAs are expressed.
- Reverse direction - search on gene name and see images of anatomy where expressed.

Age stage naming preference? not really as long as it's consistently used and comparable across species.

Data submission plans over next 6 months:
- Currently finishing up paper in next 2 weeks and will send around for review.
- High resolution immunohistochemical stains for mouse (not wildtype, cre-mediated allele) - some large (1cm in width) made with Leica confocal
- How would you like those displayed? Maximum intensity projection, click on and off different layers (4 diff channels associated). Would like simple annotation layer. Just example cells. Chad would do the annotation.
- To do that, need to submit raw files, OMI TIFs, maximum intensity projections, representational layers and then add the annotations.
- Intend to submit human images, but still waiting on the right specimens, so may not happen in next 6 months.

Comments on new site:
- Too much internal language on home page. Don't really understand what the links link to. For example, "Tutorials", I thought was about using site and "Ontology" didn't know that term when I first started in gudmap and think would confuse many new users.
- Would like Database statistics section like on old site.
- In the tutorials - images are valuable, should promote sharing and include some kind of credit or watermark that it's from gudmap. Also should include creative commons license to promote sharing with attribution.
- Would like recommended searches when you make a search
- Couldn't find project pages or how to cite GUDMAP (though both are in submenus of nav). Need to impress on people how important it is to site.
- Don't see any indication of what's different between the projects.
- Videos with narration (as discussed at last monthly meeting) would be useful.
- Don't see how to find in situ data or how to search by anatomy.
- Would like graphical interface to click on region of interest and drill down. Relying on users to know the right term - or even find it in a nested list - is dicey.
- For graphical interface, should be sagittal surface PLUS need prostate, urethra, ureters, bladder and gonads. Chad, marty and Sean could help fill in the image gaps. Kylie Georgia did great images in Little's lab but don't think she does it for hire anymore.

Comments on old site (at the hour mark):
- spent a lot of time scanning thru images
- i don’t like the way this works (had trouble doing boolean search on site now)
- not working now but what I would do is: 
  - search for ‘gene expression’ - would go in here and identify a tissue layer of interest to me. try to say what’s different about that tissue layer compared to one not of interest to me
  - Specifically: what are the types of genes that show up in early prostate epithelium that do not show up in the adjacent urethra epithelium? 
  - I would be able to drill down on a specific stage of development where I knew there was prostate. 
  - select from ontology “prostate epithelium” as tissue type and then say “i want genes strongly expressed here and not here” and pick urethra from the same timepoint. 
  - was useful for identifying genes we thought maybe were driving development of the prostate ducts. was useful but clunky and half the time didn’t work.
- re: clunky - used nested sub-terms, but then you'd have to figure out where it was organized under (is prostate under urinary tract or urethra tract? could be either). 
- liked Database Statistics box to get an idea of what was available, but should be parsed by organ.

## Tissue Hub

Not a typical user - interaction with GUDMAP is mostly sending data on tissues delivered to spokes. To that point, Luke is working with Hub - sent 20 data elements proposed for describing the tissue. Samples are barcoded and ultimately want to link tissues with experiments (submitted data) that used them.

Data submission by Tissue Hub:
After sending sample to project (on Thursday) then send clinical information to the Hub (the following Friday or Monday). It's de-identified so don't think there are privacy issues but should verify that it can be publicly viewable.

Had sent some 'dummy' data. Hub said it looked good but still waiting on policy issues. 

How much data? depends on demand but generally send 0 - 7 samples a week.

Sunny and Jackie - run kidney development labs - _do_ use the GUDMAP site, so they showed us how they use the site.

What kinds of searches do you do?
do a lot of rna-sequencing on different compartments of kidney. get a list of top candidate genes. i want to know if expressed in the cmopartment i'm interested in. look in microarray or rna-seq data. then look for where in the tissue it is by whole-mount or in-situ. 

Go to "Gene Expression Database", type in gene of interest, and find the microarray analysis, click on kidney one, and see the expression profile. Go back and look at in-situ data.

Use it in conjunction with eurexpress.org because it's the whole embryo - from one side to the other. In fact, excited about gudmap3 site because the interface looks close to eurexpress.org in the sense you can zoom in and out of high resolution images. note they liked the anatomical tree on that site that appears next to search results because it highlights anatomical regions where the gene is expressed.

what searches would you like to do but haven't been able to do
like to do batch genes - now it's one gene at a time. but may have ten candidate genes.

give a list and it spat out - 8 of these genes are in the tissue of interest.

if some way to store some of those searches in your own profile, would be good.

hongsuda: we do have a way in the new site. you can bookmark using the 'permalink' and can go back to it.

good - but still would be nice to have your recent searches, saved searches (doesn't have to be the results themselves), etc. and then share with grad students.

also if we have a gene of interest look at how much sequencing data is in db and which tissue it's expressed in. in the current site, you access the info but it's cumberson - by sample or by series. but you just want to know is this present in what age stages?

What system do you prefer for age stages? (sunder/jackie with mouse work)
typically go by embryonic day. fine to use theiler stage but would be nice to have a simple link to the equivalence in embryonic day.

Human age stage - we've been going back and forth between conceptual and gestational age. 
Some sort of clarification on that on the website would be helpful. All the investigators want 'heel-toe' measurement.
We provide conceptual or gestational AND heel-toe

Sunder and Jackie will be submitting "small RNA" or microRNA. Looks like this is a new data type for the Hub.

Comments on new site:
- Antibody information is very useful
- Eye icon on high rez image means something different than the "View" eye in search results.
- Would like heat maps to show up in search results as they do on current website
- Heatmaps look better on new site: easier to read and better laid out (labels are hard to read) - could add a legend and then use shorter terms in the labels.
- Suggest youtube tutorials
- homepage is fine. 
- navigation should be closer to existing site (ie, Gene Expressions is not under Resources)
- Data Browser links below seem fine except Mouse Strains don't fit under "Cell Lines" should maybe change to "Transgenic Lines"

Side usability notes as they used new site:
- Seemed to miss when pointing at the submenus in the navigation a couple of times
- Did not recognize that the "eye" icon was what they should click to see the detail page for a record.

Sunder and Jackie will be the contacts for future testing.

## Keast

Focus on nerves science/neuronal anatomy. Still contributing data from GUDMAP2 and then via the [SPARC](https://commonfund.nih.gov/sparc) program. Species is rat

No rat ontology available.

What kinds of searches do you perform on current site?
Use the gene expression database to search gene of interest and look if there's gene expression profile. What is there on it? is gene expressed in urinary tract, etc?

Janet notes some QC issues - in the last annual meeting there were discussions about whether to submit raw data or should it go through analysis. Thinks there should be some kind of validation of the data before uploaded to Hub.

Data submission plans over next 6 months? Still finished GUDMAP2. Edinburgh has RNA-Seq. Waiting to send any further data to new Hub. Will be images of neurons and ganglia with description and numerical data. Excited that new Hub would be able to visualize the numerical data (histogram/plots)

Uses current site:
- Gene Expression Database
- Educational tutorials (sometimes just to look up Theiler stages)
- Protocols
- Schematics are useful
- Really liked the data reports and minutes available on internal site
- Notes that QC page is only for in-situ (which was sole focus of gudmap1). It's lopsided not to have QC parameters for other data types.

Age stage: whatever naming you use is fine as long as there's an easy way to look it up or map it.

Comments on new site:
- Really like homepage. Like the whitespace, clean
- Issue with attributes in sidebar - useful ones hidden, some extraneous ones there (Date created), also seems short enough list to just display all attributes from the get go. (NOTE: Hub has deprecated this version of the sidebar - but are taking steps to make sure attributes listed in new version are logical to user).
- Like the heatmap - easier to read (tho labels are hard to read). Didn't quite understand the 'x' and 'y' coordinates at first.
- Usability note: immediately used eye/view icon as designed.
- Would like to be able to see heatmap in search results.

Contact for future testing: Janet, but Victoria will be data contact whenever there's information about data submissions.

## Li

Research focuses on morphogenesis of lower urinary tract and molecular basis of penile urethral tube formation.

What info do you need for your research?

- Expression data - especially want to know the sex of the organism after 14.5 embryonic days. Would like to see all expression data by sex and age stage, including protein expression, sutures, etc.
- Enhancer data mapped to current genomic sequence (latest release) and updated automatically. 

What kids of searches do you perform?
Keyword search on gene. Not much by anatomical structure, but that could interesting in the future.

What kinds of searches would you like to be able to perform but cannot now?
Nothing really. Though it would be interesting to be able to do more specific searches on how pathways differed in stages.

What are your data submission plans over the next 6 months?

- already have images and video to submit now. 
    - Videos: morphological transformations over developmental changes. Region of anatomy over time.
    - Images: 3-D
    - May be good for Education site
- May have transcriptome data (rna-seq)
- Some of the data may need to be embargoed.

Old site: 

Did you use the old site? How often?
Not much. But if I did use it, I would generally go to the gene expression database.

Another site I use: genepaint.org and use keyword search

Putting on your 'researcher' hat (as opposed to this project's PI), what kind of information would you find useful?

Cell type specificity for lower urinary tract. It's usually generalized, but there are 
Any microarray, for specific cell types and tissues.

Enhancers - regulatory element embedded in genome (DNA). Associated with specific genes. No standard naming. related to physical location. Range of addresses on a chromosome. Example of source for enhancer data is ENCODE.

New site:
Give us your impressions of the new homepage:
- Full name in header is too long
- Resource Links are too wordy - would like to see main category by itself as a bullet and then chunk the related links
- Don't like new pages when navigating through data browser (chaise). End up with too many tabs.
- Data: shows sex, which is good! liked external links.
- Most people will be searching specifically for data for a particular hypothesis. what would _really_ help is by showing genes' association with other genes. For a given genes, who which genes are associated with it by functionality, disease, encoder protein, pathways, etc. Li will email a website where the Hub could find this information.
- Gene search page - don't need list, just search box (ala google)
- Gene detail page is fine
- RNA-Seq example page - wanted metafile description (how the data was generated, etc). Hub pointed him to Sample Settings section and Li said that info would suffice.
- Would like more of a dashboard summarizing available data in the browser. Hub showed him a dashboard in teh chaise navigation - he said that should be the front page.

## McMahon

What kinds of searches would you like to do?
Batch: Not just one gene - 15 genes, paste those in, press enter, then get a page with the RNA-Seq profile.
Anything analytical, want to see everything, then drill down from there.

Look for genes - in situ microarray, usually not through tissue but through gene.

GUDMAP did have a batch search but it's too complicated.

On way system from MGI db ot GUDMAP but not the other way around - have to click multiple times to look.

Data submission plans?
75 TIF stacks - confocal images, AMIRA segmented subjects.
Large number mirror - 350 NIFTI
30 AVI movie files - linked to TIF/AMIRA objects
5 Excel files

Associated with age, anatomical feature, proteins and genes. 
Will work with Hub for a new data model, allow movies to be viewed in browser.

Do you use current site? Daily basis. Gene in search bar. SISH first if available, and if I see where expressed, scroll to interesting slide. Move around and zoom in and look at details
Go back to opening and search on kidney expression, see where most likely expressed.
Tried to use other search but not successful (query/browse db). Boolean search but not sure how to interpret results.
And then in cases like search bmp7 in nephro, don't trust the results. Could be annotation issue/bug.

Mouse Strains - only if question about specific gene you're not familiar with. More of a reference.

When there's a new person in the lab, send to the Developmental tutorials.

Feedback on new site:

Missing a search bar on the homepage. Emphasis on Data Browser links seems to be on wrong things - if looking at antibodies, first column shouldn't be product, should be Protein Target.

Gene search looks good. when looking at detail page, page title should have a better name. Info on details page could be condensed, images are the more important detail.
Like the heatmaps, can't read lable. Looks better.

For gene landing page - would like to search on multiple genes. You want more relevant details in the results to see if it's interesting and you want to click for more info. Would really like profile information in the results.

## Mendelsohn

What kinds of information are you interested in?

Is this gene expressed in this tissue on that day?

What kinds of searches would you like to be able to perform that you can't already?

* Boolean: E14 AND upk NOT cancer
* Link to images from journals (ie Development)

What are your data submission plans over the next 6 months?

Immunohistochemical - 3 or 4 channels 
50 images
in-site - 10-20
single-cell RNA-Seq and RNA-Seq mouse

How do you use original site?
Do use it - it's useful
Don't love the way it's set up but you can get good info from it.

Enter a search on a gene like upk1b.
Looks bad and to type in a term, it has to be exactly right
Then look at microarray, hover mouse and it tells you which structure, how much it's expressed there. Click on it to look at the distribution of the expression of the gene in different parts of the lower urinary tract timeline.

Also look at images.

What else would be good to show on the results page?
MGI is the place that has everything. GEO annotations could be good.

Pain points with current site?

It's been so long I don't use the things that were driving me crazy anymore : )

Some data could be better curated. Esp whole mount in situ hybridization data. 
Would be nice for PIs to be able to flag content that needed curation or had an issue.

Looking at gudmap3 beta:
- Pretty cool
- Slow going (cris: in chaise, there was a performance bug that's being worked out)
- Like the look of it. Much better
- Gene page - searched for a gene
- Note: clicked on 'homo sapiens' to see more results - which doesn't take you to the details page. We asked why she clicked it = "Because it's blue and looks like a link". We pointed out the eye would take her to the details page but she didn't think that would be noticed by users. Needs a better, more obvious way to choose the details for that Gene.
- Likes detail page - but couldn't see heatmap because of an ad-blocker extension she's using for Chrome (UBlockOrigin).
- What else should be on the details page? Disease or OMIM 
- don't need both 'antibody' and 'antibody test' path should be one or other (and maybe antibody test should read antibody validation)
- Use 'Mouse Lines' instead of 'Alleles' (Allele makes you think of mutation)
- Too many clicks: Had an issue with how far down you had to drill through some records to actually get to data. People want the data files asap. And downloadable data files should be higher up on page instead of scrolling through so much info to get to it.
- .czi isn't a great format (nobody can't open it) - but there should be a thumbnail (screenshot) so you can have an idea of what's in it before you take trouble to download.
- Metadata shown is good. But wouldn't put it on top - would put it below. Data you want people to click on should be on top. The way they presented the microarray in current gudmap search results, it immediately gives a sense of what's there.

## Cohn

With Brooke and Emily Merton (data submitter)

Typically curious where a gene is expressed

Interested in in-situ hybridized, immunofluorescence

Microarray is of limited to no use. 3D data will be useful at some point.

Biggest issue is lack of data on gene expression. Shouldn't have to go to another site when GUDMAP is missing a expression data for a gene. But until that data is added to the gudmap site, could at least still show a result for that gene with links to where there is info on external resources: Allan Brain Atlas, Mouse Atlas, etc. Be a gateway. It should appear in the search results.

Data submission plans - over next 6 months
Unfortunately because of issues getting tissue, probably not in the next 6 months. But after that timeframe hope to provide:
1. RNA-Seq
2. histological data - sending slides to USC scanner and from there to the Hub (just like Andy's data)
3. microCT data

How would you typically search for data on original site?
Search gene, see where expressed. Never use the Expression Profile column. look for expression images, in situ data. If no in-situ, may go to the array data to see where expressed.

What I like about current site - covers our area of domain. expression raw data. gene expression patterns.

Brooke searches differently - not by gene. Instead clicks on the microarray link in Database Statistics. Compares what's found in bladder with what's in urethra. Show all related genes and see which genes are common to both. Can do that in current gudmap but it's not intuitive.

(Bluejeans issues - had to stop for a few minutes)

Brooke: Wants to find part of the anatomy on a heatmap: anatomical region vs time point

Marty says no one cares about the Database Statistics section of the current homepage. Too much distracting info.

Checking out gudmap3 beta
- Accessible info is better, more intuitive
- Where's the search box? Want as few clicks as possible. Jump straight into a gene search.
- Gene page - don't like it when it gives you results before you hit the button (auto-suggest/complete)
- Gene detail page. Looks much better. nice! Likes external sources link.
- Might want to discuss with PIs _if_ we want to link to external gene expression databases. Link to MGI might be enough.
- When there's a heatmap (microarray) on a gene detail page, there should be metadata for it. Who it came from, which lab produced it, info about the experiment, etc. 
- Brooke: on gene detail would like to know if there's a mouse model (mouse strain).
