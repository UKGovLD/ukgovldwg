---
title: What is Linked Data
layout: miniguide
author: John Goodwin
abstract: a brief introduction to the concept of Linked Data.
published: true
---

In the early 1990s there began to emerge a new way of using the internet to link documents together. It was called the World Wide Web. What the Web did that was fundamentally new was that it enabled people to publish documents on the internet and link them such that you could navigate from one document to another.

Part of Sir Tim Berners-Lee’s original vision of the Web was that it should also be used to publish, share and link data. This aspect of Sir Tim’s original vision has gained a lot of momentum over the last few years and has seen the emergence of the Linked Data Web.

The Linked Data Web is not just about connecting datasets, but about linking information at the level of a single statement or fact. The idea behind the Linked Data Web is to use URIs (these are like the URLs you type into your browser when going to a particular website) to identify resources such as people, places and organisations, and to then use web technology to provide some meaningful and useful information when these URIs are looked up. This ‘useful information’ can potentially be returned in a number of different encodings or formats, but the standard way for the linked data web is to use something called RDF (Resource Description Framework).

RDF is a standard from the World Wide Web Consortium (W3C) and it provides a very simple way of encoding data that is based around making a series of statements about resources. These statements relate one object to another object via some kind of property. Formally these statements take the form subject-predicate-object and are known as ‘triples’. A couple of simple examples of triples would be “John is based near Southampton” and “John works for Ordnance Survey”. However, in the RDF the resources John, Southampton and Ordnance Survey would be identified by a URI as would the predicates “based near” and “works for”.

Using URIs the triple “John is based near Southampton” would look something like:

http://www.johngoodwin.me.uk/me

       http://xmlns.com/foaf/0.1/based_near

                 http://data.ordnancesurvey.co.uk/id/7000000000037256

and the triple “John works for Ordnance Survey” would look something like:

http://www.johngoodwin.me.uk/me

    http://www.intelleo.eu/ontologies/organization/ns/worksFor

         http://data.ordnancesurvey.co.uk/id/ordnancesurvey

In essence this is all there is to RDF data – a series of statements in the form of triples providing information about a given resource. One way to think about RDF is that it is to the web of data what HTML is to the web of documents. Just as HTML provides a standard way of linking documents on the web, so RDF provides a standard way of linking data on the web.

When it comes to the linked data web it is important to used HTTP URIs to identify resources. The use of HTTP URIs means that the URIs can be ‘looked up’ or dereferenced by people and user agents (such as software applications) and useful information returned to the client.

Consider, for example, the linked data published by Ordnance Survey. Ordnance Survey has published linked data about administrative and voting geographies (this includes things like counties, districts, ward, constituencies etc.), along with linked data for postcodes. Each administrative region and postcode is Great Britain is now identified by a URI. When you look up the URI for The City of Southampton (http://data.ordnancesurvey.co.uk/id/7000000000037256) you’ll either get back an HTML page describing Southampton (if visiting from a web browser) or an RDF document describing Southampton (if accessing via a linked data client). The RDF document returned will contain a number of triples about Southampton, listing (for example) all of all the wards contained in Southampton along with the counties and unitary authorities that Southampton is adjacent to. Similarly, dereferencing a postcode URI (e.g. http://data.ordnancesurvey.co.uk/id/postcodeunit/SO160AS) will return triples describing that postcode such as the ward and district the postcode is in along with a representative coordinate for that postcode.

## To summarise:
the basic idea behind the linked data web is to use web technologies to lower the barriers to integrating disparate datasets. Key to this is the use of a common standard data model (RDF) and the use of URIs as global identifiers for resources.

## What can you do with Linked Data?

A number of years ago the government wanted to have an application that enabled them to identify centres of excellence for research around the country. To answer this challenge Talis, Iconomical and the data.gov.uk team got together to build a Research Funding Explorer. They decided to show how linked data techniques could bring real benefits when it comes to joining and analysing data from a number of different sources. The initial problem they were faced with was that these datasets were typically encoded in large spreadsheets and scattered across a number of government departments and research funding bodies. In order to integrate this data they converted the spreadsheets to RDF and made reference to URIs for objects already published as part of the government open data initiative. Once the data was converted into RDF it was possible to load it into a triplestore (databases for RDF are know as triplestores).

The first version of the application allowed a user to browse funded research projects by subject and organisation. Furthermore, the original work contained a geographical element which allowed you to see which projects were being funded in which region.

Following this link we can see which projects are being worked on by institutions in the South East of England, and how much funding they are receiving. However, it would arguably be useful if you could also view the geographic distribution of projects at a more fine grained level. In this case it was possible to enable a more fine grained view can be made possible by linking the data to Ordnance Survey’s linked open data about postcodes.

## Here’s how…

In the original data the postcode is recorded for each institution. The postcode is captured simply as text. However, enhancing the original data to link to a postcode URI means the original data has the potential to contain a lot more information. Once the URIs for each postcode is in place it is a relatively simple matter of using some simple code to follow that link, dereference the post code URI and ingest the linked data for that postcode into the triplestore. So just as humans will follow links between documents on the web to gain more context and information this simple application has followed links on the linked data web to provide more context and information. Because the postcode linked data provides a look up between postcode and region, it was possible to enrich the original data with knowledge about the ward, district and county (where applicable) for each institution. This means it is now possible to analyse research funding by local authority area as well as European region.

Using the spatial relationships in the Ordnance Survey linked data means it is possible to start doing more complex analysis. For example, a user could compare funding in one region with funding in its neighbouring regions or use the containment relationships to aggregate the information up to coarser grained geographies.

This simple example shows that using linked data techniques to bring a number of relatively simple datasets together can start to yield real benefits. Imagine the possibilities…