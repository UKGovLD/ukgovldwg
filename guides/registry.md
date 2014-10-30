---
title: Linked Data Registry
layout: guides
author: Dave Reynolds
abstract: "The Linked Data Registry enables organizations to collaboratively publishing and maintain reference data, such as a code lists, as persistent resolvable URIs. This guide introduces the notion of the registry and provides links to documentation and running examples."
---

## Reference data

A key enabler for shareable, reusable open data is accessible reference data. By *reference data* we mean the standardized terms used to identify "things" in the data - things such as codes, spatial objects, namespaces, units of measure, substances, methodologies, organizations and general vocabulary elements. Most data sets make use of such identifiers and to safely interpret the data we need to know what they mean. To enable data sets to be combined or compared we need to reuse, or at least map between, these reference identifiers.

Such reference data needs to be:

   * independent of a particular data system (global)
   * persistent
   * interpretable (*resolvable*)

The UK Standards board has adopted HTTP URLs as the basis for all such persistent, resolvable identifiers.

This then leads to the challenge of how organizations can publish and maintain their reference data as resolvable URIs. 

   * How can multiple organizations share an authoritative namespace (such as `location.data.gov.uk`)? 
   * How can non-experts generate machine-readable descriptions of the identifiers? 
   * How can authoritative closed lists of identifiers be created - so that data users can validate whether a given identifier is or is not on a list endorsed for a particular purpose?

## Linked Data Registry

The Linked Data Registry is a tool to manage such reference data, particularly things like code lists. 

It provides a service to create and manage controlled, authoritative lists of identifiers as URIs. The identifiers in these lists may be *external* to the registry (maintained by a third party) or may be managed within the registry namespace. For such *managed* identifiers then the registry stores core data so that the identifiers resolve and provides for management and maintenance of that data. It allows different groups to publish identifiers within a shared namespace.

In addition to the core services of list management, and supporting managed identifiers, then the Linked Data Registry provide a number of ancillary services including versioning of identifiers, search and discovery, validation and general namespace delegation.

The Linked Data Registry, developed under the sponsorship of the UKGovLD Working Group, comprises:

   * an open [design](https://github.com/UKGovLD/ukl-registry-poc/wiki) including an [information model](http://www.epimorphics.com/public/vocabulary/Registry.html) and [API](https://github.com/UKGovLD/ukl-registry-poc/wiki/Api)
   * an open source reference [implementation](https://github.com/UKGovLD/registry-core)
   * a number of customized, deployed instances

## More information

For more information on the Linked Data Registry see:

   * [Documentation](https://github.com/UKGovLD/ukl-registry-poc/wiki) 
   * [Introductory webinar slides](http://www.slideshare.net/der42/registry-webinar)
   * [Technical training slides](http://www.slideshare.net/der42/registry-technical-training)

## Deployed examples

Service | Status | Deployment sources
---|---|---
[Environment registry](http://environment.data.gov.uk/registry/) | Alpha pilot | [registry-deploy-env](Source)
[Location registry](http://location.data.gov.uk/registry/) | Alpha pilot | [registry-deploy-loc](Source)
[Training registry](http://registry-training.epimorphics.net/registry) | Training only | 
[WMO codes](http://codes.wmo.int/) | Pilot |

## Supporting utilities

In addition to the Linked Data Registry itself then UKGovLD has developed a supporting service to allow conversion of CSV data to RDF format suitable for uploading to the registry.

   * Pilot service:  [registry-util](http://environment.data.gov.uk/registry-util/)
   * Source: [registry-dcutil](https://github.com/UKGovLD/registry-dcutil)
   * Documentation: [Technical training slides](http://www.slideshare.net/der42/registry-technical-training)
