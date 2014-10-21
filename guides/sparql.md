---
title: SPARQL
layout: miniguide
author: Leigh Dodds
abstract: "SPARQL is a query language used to interact with RDF databases"
---

SPARQL is a query language used to interact with RDF databases or "triple stores". While Linked Data supports the publication and consumption of data in a variety of data formats using simple HTTP requests, there is often a need to perform custom queries over a dataset. Many Linked Data datasets also expose a query API or "SPARQL endpoint" that allows SPARQL queries to be executed over the dataset, with results returned in a variety of RDF and tabular response formats.

By using SPARQL data consumers can query RDF datasets in more flexible ways. By providing a SPARQL endpoint data publishers can expose a single API that provides consumers with a sophisticated set of tools for interacting with their data.

## The SPARQL Specifications

SPARQL actually consists of a set of W3C Recommendations that together specify the complete query language, response formats and API. The core specifications include:

* The [SPARQL Query Language](http://www.w3.org/TR/sparql11-query/) specification which describes the syntax of SPARQL queries
* The [SPARQL Protocol](http://www.w3.org/TR/sparql11-protocol/) which defines a simple API for submitting SPARQL queries over HTTP
* The SPARQL [XML](http://www.w3.org/TR/rdf-sparql-XMLres/), [JSON](http://www.w3.org/TR/sparql11-results-json/) and tabular [CSV and TSV](http://www.w3.org/TR/sparql11-results-csv-tsv/) response format specifications define simple data formats to be used to return query results

These specifications cover the elements of SPARQL which will be most relevant for consuming data on the web from existing SPARQL endpoints. The additional specifications cover extra features such as [updating RDF triple stores](http://www.w3.org/TR/sparql11-update/), describing [SPARQL endpoint capabilities](http://www.w3.org/TR/sparql11-service-description/), and [federating SPARQL queries](http://www.w3.org/TR/sparql11-federated-query/). Many of these extra features were added during the work to develop SPARQL 1.1 which was completed in 2013.

## Types of SPARQL Query

The SPARQL query language defines a number of powerful features for querying RDF graphs. Unlike SQL, for example, which defines only a single type of query to extract data (`SELECT`), SPARQL defines four different types of query:

* `ASK` queries are used to to test whether a dataset contains individual data points, or particular patterns of data. These queries are useful for checking if a dataset contains data about a resource, or for validating the structure of the dataset
* `SELECT` queries, similar to their SQL equivalents, allow a tabular set of results to be extracted from a graph
* `CONSTRUCT` queries extract custom RDF graphs from a dataset. This type of query can be useful for extracting subsets of a dataset for local use, e.g. for data synchronization. The ability to generate new triples also allows CONSTRUCT queries to be used for data transformation and normalisation
* `DESCRIBE` queries also extract RDF graphs, but in this case defer to the endpoint to provide a default description of the specified resource(s). These queries are useful for prototyping and data exploration where the exact form of the graph may not be known

Combined together these different forms of queries provides data consumers with a number of options for extracting data from a dataset. RDF applications can use `CONSTRUCT` and `DESCRIBE` queries to extract data in their preferred native formats, whilst other applications can use `SELECT` queries to slice up an RDF graph into simpler tabular views.

The majority of SPARQL endpoints support not just the standard range of RDF serializations but also the standard XML, JSON and CSV formats that allow data from SPARQL endpoints to be integrated into a variety of client-side tools.

## Further Reading

* The Apache Jena [SPARQL tutorial](http://jena.apache.org/tutorials/sparql.html) introduces the major features of the query language
* [SPARQL by Example](http://www.cambridgesemantics.com/en_GB/semantic-university/sparql-by-example) provides an example driven tutorial to the language
* [SPARQL by Example Cheat Sheet](http://www.slideshare.net/LeeFeigenbaum/sparql-cheat-sheet) is a handy reference to the important elements of SPARQL syntax


