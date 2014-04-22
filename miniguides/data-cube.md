---
title: Data Cube Vocabulary
layout: miniguide
author: Dave Reynolds
abstract: "People often think of linked data as being a way to connect descriptions of things into a graph of relationships, for example to link a school to the organization that oversees it. So how do we deal with data which is naturally presented as tables and charts, things like official statistics or environmental measurements?"
---

People often think of linked data as being a way to connect descriptions of things into a graph of relationships, for example to link a school to the organization that oversees it. So how do we deal with data which is naturally presented as tables and charts, things like official statistics or environmental measurements? Is linked data of any use in that case? If so, how do we approach the problem?

## Why?

In fact the same values that apply to linked data in general apply to such tabular data.

Firstly, it allows us to integrate, compare and slice across data sets. It enables us to publish the information model along with the raw data and to use common terms (identified by URIs) for the dimensions and units in our data sets and for the non-numeric values (e.g. for geographic regions or organizations). This in turn allows us to compare and link reliably across data sets in ways that are not possible with simple spreadsheets.

Secondly, by publishing as linked data we give web addresses to the data sets, data slices and individual observations. This opens everything out. It makes it possible to annotate, explain and qualify the values. For example, to explain why a given payment is unusual or to reference the measurement methodologies for a particular year of samples to explain why they might not be comparable with another year. It allows us to link to provenance information about where the data came from and allows re-users of our data to link back to our sources laying down a trail of evidence to support decisions based on the data.

## How?

To achieve this we need a standardized vocabulary for representing such regular data sets and their structure. This is the RDF Data Cube Vocabulary. 

![Summary picture of the simple core of the vocabulary](http://www.epimorphics.com/web/sites/default/files/qb-sample.png)

At the heart of the vocabulary is the concept of _dataset_ which is a collection of _observations_. The observations are organized along a set of _dimensions_ (e.g. time, geographic region) and each observation has one more associates _measurements_ (e.g. _population_ or _air quality classification_). To reliably interpret the measurements you may need other information such as the units of measurement or the measurement process used, these annotations are termed _attributes_. All of the information defining the structure of the dataset is given in a _data structure definition_ which means that RDF Data Cubes are self describing - from an observation you can find the enclosing data set and the the corresponding definition of its structure.

It is based on the core information model of SDMX, a standard for exchange of aggregate statistical information, but is not limited to such data. It can be used for any sort of regular data. 

The vocabulary was first created in 2010 under the initiative and sponsorship of John Sheridan (The National Archive) and developed by Dave Reynolds (Epimorphics), Richard Cyganiac (DERI) and Jeni Tennison (now ODI) with sage guidance from Arofan Gregory. After three years of application experience, and some small adjustments to vocabulary, it has recently become a full [W3C Recommendation](http://www.w3.org/TR/vocab-data-cube/). 

There have been a wide variety of [implementations](http://www.w3.org/2011/gld/wiki/Data_Cube_Implementations) of Data Cube including publishing statistical, environment and observational measures together with tools for data conversion, data validation and visualization. 