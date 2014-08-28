---
title: Ordnance Survey Linked Data
layout: casestudy
author: John Goodwin
abstract: A case study describing the Ordnance Survey Linked Data Platform
---

In the early 1990’s there began to emerge a new way of using the internet to link documents together. It was called the World Wide Web. What the Web did that was fundamentally new was that it enabled people to publish documents on the internet and link them such that you could navigate from one document to another. Part of Sir Tim Berners-Lee’s original vision of the web was that it should also be used to publish, share and link data. This aspect of Sir Tim’s original vision has gained a lot of momentum over the last few years and has seen the emergence of the Linked Data Web.
Link pattern

The Linked Data Web is not just about connecting data sets, but about linking information at the level of a single statement or fact. The idea behind the linked data web is to use URIs (these are like the URLs you type into your web browser when going to a particular website) to identify things such as people, places and organisations, and use web technology to provide some meaningful and useful information when those URIs are looked up.
Ordnance Survey and Linked Data

Ordnance Survey’s research department has been interested in Linked Data for quite some time, and the release of OS OpenData meant that the fruits of these efforts could finally be realised, providing Ordnance Survey an opportunity to make a major new contribution to the Linked Data Web.

As a first toe in the water Ordnance Survey decided to produce a gazetteer of the administrative regions of Great Britain. Each region is given a unique identifier in the form of a URI and described in terms of its name and the spatial relationships it has to other regions. So, for example, if you look up The City of Southampton (identified by the URI http://data.ordnancesurvey.co.uk/id/7000000000037256) you’ll find a list of all the wards contained in Southampton along with the counties and unitary authorities that Southampton is adjacent to.

Ordnance Survey has also published URIs for every postcode in Great Britain and linked these to URIs for the administrative regions. The URI for our head office's postcode (SO16 0AS) is:

http://data.ordnancesurvey.co.uk/id/postcodeunit/SO160AS

Looking this up you’ll see that Ordnance Survey is based in the district of Test Valley and the county of Hampshire.

This offers great potential to data publishers. By linking to identifiers for places and postcodes in your data you can enrich the information you hold. Imagine you have a list of schools and their postcodes. By connecting to the URIs for those postcodes you have a whole new way to view and analyse your data. Through the link to the postcode you now know the ward, district and county those schools are in. This is a very simple example of how merging two sets of linked data can deliver benefits. 

Ordnance Survey first published its linked data in April 2010 and have seen a continued growth of the use in government and research. Last year the linked data platform was relaunched with a number of improvements:

    Developed a data hub that provides access to all our Linked Data datasets, with integrated search to enable anyone to easily locate resources of interest.
    Embedded OS OpenSpace maps to show the geographic location chosen.
    Separate datasets, which will allow you to narrow down your searches. For example, if you are looking for postcode information, you can query just the Code-Point Open Linked dataset.
    Improved metadata for each dataset such as publication dates, licensing terms and coverage.
    SPARQL 1.1 compliant endpoints for all datasets, which provide more functionality for querying our Linked Data.
    Redesigned search API based on the OpenSearch specification and with support for geography based queries.
    Support for the Open Refine Reconciliation API, which will allow you to more easily link your data with ours.
    All new API documentation and interactive tools for all API’s, including integrated example resources and queries.
