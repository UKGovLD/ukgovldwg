---
title: The Open Data Rights Statement Vocabulary
layout: miniguide
author: Leigh Dodds
abstract: "It is important that Open Data is clearly licensed so that consumers can understand any requirements that apply to re-use of a dataset. The rights statement vocabulary supports publishing licensing metadata in machine-readable formats"
---

It is important that Open Data is clearly licensed so that consumers can understand any requirements that apply to re-use of a dataset. For example whether the data publisher has requested attribution when their data has been re-used. 

The [Open Data Rights Statement](http://schema.theodi.org/odrs/) (ODRS) vocabulary supports the publication of machine-readable descriptions of licensing information. The vocabulary is useful for both data publishers and data consumers:

* data publishers can use the vocabulary to publish clear machine-readable information about the licence, attribution requirements and copyright notices associated with their datasets
* data re-users can apply this data to automatically create and format attribution statements and display copyright notices

Machine-readable licensing information also supports dataset discovery, allowing data aggregators to provide search facilities that use this data to guide re-users towards Open Data, e.g. by filtering based on licence, and in the clear displaying of re-use information.

## Rights Statements

The ODRS vocabulary is very simple and focuses on supporting the publication of "Rights Statements". A Rights Statement is a resource that describes the relationship between a Dataset and its Licence(s). A dataset may be associated with multiple licences which separately cover re-use of the data in the dataset, and its content (e.g. text and descriptions). A Rights Statement can also be used to capture additional context that is relevant to the re-use of a dataset.

A Rights Statement may typically include some or all of the following information:

* A reference to a Dataset Licence
* A reference to a Content Licence (if, and where applicable)
* Copyright notices, that should be referenced or displayed by re-users of the dataset
* Guidance on the correct means of attributing the source of the data used in an application
* Pointers to further information relevant to data consumers, e.g. further guidance on re-use such as how to acquire additional rights

This information is usually provided only in human readable documentation. But providing a basic machine-readable description of this information, re-users can be better supported in finding the information they need and, importantly, in ensuring they can comply with licensing terms.

## Applying the Vocabulary

The vocabulary has been designed to be easily applicable in a variety of circumstances, including describing datasets in a data catalog as well as requests for Linked Data or to other APIs

The [specification](http://schema.theodi.org/odrs/) of the vocabulary is supported by two guides:

* The [Publishers Guide](http://theodi.org/guides/publishers-guide-to-the-open-data-rights-statement-vocabulary) provides a thorough introduction to the vocabulary and includes a variety of examples that show how to apply the vocabulary to real-world data.
* The [Re-users Guide](http://theodi.org/guides/odrs-reusers-guide) explains to data consumers how they should use this information in their applications, e.g. to support automated generation of attribution links

A set of [standalone examples](https://github.com/theodi/open-data-licensing/tree/master/examples) are also available that illustrate how to use the vocabulary in a number of different formats

## Further Reading

The [Open Data Institute](http://theodi.org/) have published some introductory guides on data licensing. This provides useful background for anyone publishing or consuming open data. There are separate guides that provide:

* A [Publisher's Guide to Open Data Licensing](http://theodi.org/guides/publishers-guide-open-data-licensing), and
* A [Re-users Guide to Open Data Licensing](http://theodi.org/guides/reusers-guide-open-data-licensing)





