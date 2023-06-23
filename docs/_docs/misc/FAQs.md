---
title: Frequently Asked Questions
permalink: /docs/faqs/
---


(Note: This page is a draft in progress)

## What are "RID"s and how can I use them?

The RID column for a data record is the "resource identifier" which is a permanent, citable identifier for this data. 

To reference this data, you would use `GUDMAP:{RID}` or `http://gudmap.org/id/RID`, where "RID" is the the value of the RID field.

## What is a data collection?

A data collection is a customized set of data that you can create to cite data for a publication, share an experiment with a collaborator or otherwise create a specific set of data that can be permanently cited. For more information, see [Create citable datasets](/docs/create-citable-datasets/).

## What is Globus?

GlobusID refers to the account management and authentication system we use, powered by Globus Online. Globus is a non-profit service for the research community operated by the University of Chicago and is a powerful data transfer and authentication system designed for performance, reliability and scalability. 

We are using their very secure authentication system that also works securely with other Identity Providers such as Google, ORCID and the InCommon federation to manage your login account.

You can find [more information about Globus  here](https://docs.globus.org/faq/security/#what_is_globus_id). 

You can find specific information about [accessing ATLAS-D2K resources here](/docs/accessing-gudmap-and-rbk-resources).


## How do I perform a batch search?

A batch search (or batch query) allows you to do things like filter the data for a whole set of genes. For instructions, go to the [Batch Query page](/docs/batch-query).

## How should I include data citation in my ATLAS-D2K papers?

The data citations in this paper follow current best practice by providing  actionable,  permanent global identifier, a DOI.  The resolver for this DOI is maintained by DataCite, which also maintains basic citation metadata about the referenced data collection.  The DOI is guaranteed to never change, and to alway have the citation metadata and is supported by a business model that these conditions will hold even if DataCite ceases to exist.
 
One of the functions of the DOI resolver is to redirect to the dataset landing page, which is hosted in GUDMAP.  GUDMAP makes no assurance that the current URL to the landing page will remain unchanged or even work in the future.  If it should change GUDMAP  will update the redirect in the DOI so that citations to the DOI will continue to work and the correct landing page will be located.  Hence it is essential that the proper DOI citation be used in the paper, and not the URL for the redirect.
