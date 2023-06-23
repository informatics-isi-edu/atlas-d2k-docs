---
title: Data Submission Dashboards (Internal only)
permalink: /docs/data-submission-dashboards-internal-only/
---

Note this page describes a feature only available to those with the proper permissions.

In the ATLAS-D2K data browser, there is a menu item "Dashboards (requires login)" that offers views for ATLAS-D2K. When you click either of those links (and login if you're not already - requires membership in the [kidney-writers group](https://app.globus.org/groups/af0b4010-5b75-11e6-9575-22000aef184d/about)), you'll be taken to a matrix of data records by PI and Data Type and indicating [curation status](/docs/curation-workflow) (_In Preparation_, _Hub Attention_, _Released_, etc).

This data works like other data where you can use the filtering sidebar to narrow down the results. 

## Finding and logging in to the Dashboard

First you need to get to the Data Browser part of the site. Note you can enter either from gudmap.org or rebuildingakidney.org. In either site, if you're coming from the homepage, for example, you need to click on one of the data links (ie, Search by Gene or Protocols) to get to the Data Browser part of the site. 

From there, choose "Dashboards (login required)" > "GUDMAP Monthly Submission Dashboard". 

If you are not already signed in, you'll see a popup window with "Item Not Found" message. Make sure to click the "Please login" link. You'll probably see the window go blank as the system logs you in in the background.

## To view all data released by a particular lab (requires knowing the contact PI):

We'll use Andy McMahon's lab as an example. His lab has data in both ATLAS-D2K, so let's say you wanted to know about the data he released on GUDMAP. 

First, make sure that the Consortium is chosen (it should be, but you'll see the facet for "Consortium: GUDMAP" above the search results).

In the left sidebar, make sure the Principal Investigator facet is open (click the > arrow to expand it if needed) and choose Andrew McMahon.

image TBD

The search results will display all the data the McMahon has submitted by month and data type.

screenshot TBD

You can sort a column by clicking the up/down arrows next to the column name.

Next to each data type, you'll find columns related to the available Curation statuses.

* Total - This indicates all of the records submitted regardless of curation status.	
* Released 	
* In Preparation 	
* PI Review 	
* Submitted 	
* Biocurator Review 	
* Hub Attention 	
* Amendment 	
* Embargoed 

## Narrow down by month

In the left sidebar, you'll find the "Month" facet. It uses values of _year-month_ - ie, 2018-09. Use this to specify a date range for data submitted.

for example, to see data submitted by the McMahon lab for GUDMAP for the year 2018 to date, you would use the filters described above (principal investigator = Andrew McMahon, consortium = GUDMAP) and then choose all the month values that include 2018. Note, you may need to click "Show Details..." to see all the dates, then type 2018 to only show values for 2018. Then click "All" in the column header above the checkmarks AND the Submit button in the upper right corner.

Note that the months you can check will only be months where the McMahon lab had selected data.

screenshot

## To get data record totals for Fiscal Year Reporting

Here we'll total up all data records for the Fiscal Year 2018 for GUDMAP.

1. Choose the GUDMAP Dashboard link.
2. In the _Months_ facet, choose all the months from September through Aug. For example, for FY 2018, that would be 2017-09 through 2018-08.
3. In the _Data Types_ facet, click "Show Details..." to open the modal window. Click "All" to select them all and then de-select the checkmark for "Data Collections" (these are containers of existing data and should not be counted). Click Submit.
4. In the upper right corner, click "Download CSV".
5. Open the file in a spreadsheet app and add up all the numbers in the _Total_ column. This will be the total number of data records for Fiscal Year 2018.


