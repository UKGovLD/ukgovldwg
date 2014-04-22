---
title: Organization ontology
layout: miniguide
author: Dave Reynolds
abstract: "The ontology is designed to enable publication of information on organizations and organizational structures including governmental organizations. It provides a generic, reusable core ontology that can be extended or specialized for use in particular situations."
---

Important information, both public sector and within enterprises, relates to organizations and organizational units. Yet when the UK data.gov.uk initiative began there didn't seem to be a satisfactory common vocabulary for presenting such information in linked data. Under the sponsorship of John Sheridan (The National Archive) a simple, extensible vocabulary was developed to address this - the _Organization ontology_ or _ORG_ for short.

The organization ontology has been developed and standardized within the W3C Government Linked Data working group and has recently become a full W3C [recommendation](http://www.w3.org/TR/vocab-org/).

The ontology is designed to enable publication of information on organizations and organizational structures including governmental organizations. It provides a generic, reusable core ontology that can be extended or specialized for use in particular situations.

The ontology gives terms to support the representation of:

* an organization - including its purpose, classification and possible identifiers
* organizational structure - including decomposition into sub-organizations and units
* membership and reporting structure within an organization - including roles, posts, and the relationship between people and organizations
* location information - including sites or buildings, locations within sites
* organizational history 

This coverage corresponds to the type of information typically found in organizational charts. 

<figure id="summary">
	<a href="http://www.w3.org/TR/vocab-org/img/OrgOntology20130502.png"><img src="http://www.w3.org/TR/vocab-org/img/OrgOntology20130502.png" alt="A pictorial summary of the ontology"></a>
	<figcaption>A pictorial summary of the ontology (<a href="http://www.w3.org/TR/vocab-org/img/OrgOntology20130502.png">click to enlarge</a>)</figcaption>
</figure>

The ontology is aimed at supporting linked data publishing of organizational information across a number of domains. It is designed to allow domain-specific extensions to add specific classification of organizations and roles, as well as extensions to support neighbouring information such as organizational activities. Users of the ontology are encouraged to define profiles which strengthen interoperability by specifying particular controlled vocabularies to use for these concepts.

There have a broad range of [implementations](http://www.w3.org/2011/gld/wiki/ORG_Implementations) using the Organization Ontology including its use in the UK Cabinet Office publication of organograms.