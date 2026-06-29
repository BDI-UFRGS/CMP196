# MARC-21-BFO: MARC 21 with Basic Formal Ontology

[![License: GPL v2](https://img.shields.io/badge/License-GPL%20v2-blue.svg)](LICENSE)
[![Ontology IRI](https://img.shields.io/badge/PURL-Ontology%20IRI-orange)](http://purl.org/marc-21/ontology)
[![BFO 2020](https://img.shields.io/badge/Foundation-BFO%202020-green)](http://purl.obolibrary.org/obo/bfo.owl)

An ontological serialization and alignment of the **MARC 21 Bibliographic Format** with the **Basic Formal Ontology (BFO 2020)** and related OBO Foundry ontologies, following realism-based ontology engineering principles.

---

# Provenance

The ontology was developed at Universidade Federal do Rio Grande do Sul (UFRGS)/Master Degree

Development period: 2026

Ontology engineers:

* Andrew Paes da Silva (https://orcid.org/0009-0006-3997-2300)
* Mara Magda (https://orcid.org/0000-0002-9595-4207)

Academic advisor:

* Prof. Dr. Mara Abel

# Overview

The MARC21-BFO Ontology is an ontology engineering project developed to provide a semantically rigorous representation of bibliographic catalogs, MARC 21 records, library holdings, cataloging activities, and circulation processes.

The ontology combines concepts from:

* MARC 21
* FRBR
* Basic Formal Ontology (BFO)
* Information Artifact Ontology (IAO)
* Relations Ontology (RO)

The objective is to bridge the gap between traditional bibliographic metadata structures and formally grounded representations of real-world entities.

This project is being developed as part of an academic research initiative in the Graduate Program in Systems Analysis and Development at Unisinos.

---

# Purpose and Scope

Traditional bibliographic systems are primarily designed as metadata exchange structures. Although MARC 21 successfully represents bibliographic records, it does not explicitly distinguish between:

* Physical entities existing in reality;
* Information artifacts describing those entities;
* Social roles played by agents;
* Processes occurring over time.

This ontology addresses that limitation by grounding bibliographic concepts within the BFO framework.

The model distinguishes:

## Physical Reality

Examples:

* Persons
* Libraries
* Publishers
* Physical books
* Servers and storage devices

## Informational Reality

Examples:

* Bibliographic Works
* Expressions
* Manifestations
* Catalogs
* MARC Records
* Loan Records

---

# Objectives

The ontology seeks to:
* Represent bibliographic resources according to FRBR concepts:
  * Work
  * Expression
  * Manifestation
  * Item
* Model MARC 21 bibliographic records as Information Content Entities.
* Represent library organizations, users, catalogers, and publishers.
* Model cataloging and circulation processes.
* Provide semantic interoperability with OBO Foundry ontologies.
* Support future applications involving:
  * Knowledge Graphs
  * Semantic Search
  * Linked Open Data
  * Digital Libraries
  * Research Data Integration

---

# Methodological Approach

This project follows the principles of **Realism-Based Ontology Engineering**.

Instead of treating concepts merely as labels or database fields, entities are classified according to their mode of existence in reality.

The ontology adopts the taxonomic structure of BFO.

## Independent Continuants

Autonomous entities that exist independently.

Examples:
* Organization
* Library
* Publisher
* Person
* BibliographicItem
* CatalogCarrier

## Generically Dependent Continuants

Information entities that require a material bearer but may be copied across different carriers without losing identity.

Examples:
* BibliographicWork
* BibliographicExpression
* BibliographicManifestation
* Catalog
* BibliographicRecord
* LoanRecord

## Specifically Dependent Continuants

Entities that inhere in other entities.

### Roles

Examples:
* AuthorRole
* CatalogerRole
* ReaderRole

### Qualities

Examples:
* RecordCompleteness
* CatalogingStatus
* ItemAvailability

## Occurrents

Temporal entities unfolding through time.

Examples:
* CatalogingProcess
* LoanProcess
* RecordUpdateProcess

---

# Ontological Foundations

## Basic Formal Ontology (BFO)

Provides the upper-level ontology structure.
Official website: https://basic-formal-ontology.org
Imported ontology: http://purl.obolibrary.org/obo/bfo.owl

---

## Information Artifact Ontology (IAO)

Provides support for:
* Information Content Entities
* Documents
* Records
* Identifiers

Imported ontology: http://purl.obolibrary.org/obo/iao.owl

---

## Relations Ontology (RO)

Provides standardized relations such as:
* has role
* bearer of
* participates in
* realizes
* concretizes

Imported ontology: http://purl.obolibrary.org/obo/ro.owl

---

## FRBR Conceptual Model

Provides the conceptual bibliographic structure:
```text
Work
  ↓ realized by
Expression
  ↓ embodied in
Manifestation
  ↓ exemplified by
Item
```

---

## MARC 21

Machine-Readable Cataloging standard maintained by the Library of Congress.

Official documentation: https://www.loc.gov/marc/

---

# Competency Questions

The ontology is intended to answer questions such as:
* Which Person authored a given Work?
* Which Manifestation embodies a given Expression?
* Which BibliographicRecord describes a specific Manifestation?
* Which Library owns a specific BibliographicItem?
* Which Reader borrowed a given Item?
* Which Catalog contains a specific BibliographicRecord?
* Which CatalogingProcess generated a given record?
* What is the current availability status of an Item?

---

# Software and Environment Setup

## Protégé

The ontology is developed using Protégé.

Download: https://protege.stanford.edu/

Recommended version:
```text
Protégé 5.6+
```

---

## Requirements

* Java 8 or higher
* Internet access for first-time ontology imports
* HermiT Reasoner (recommended)

---

# Getting Started

Clone the repository:
```bash
git clone https://github.com/andrew-paes/marc-21-bfo.git
```

Open in Protégé:
```text
ontology/marc21.owl
```

Verify that imported ontologies load successfully:
* BFO
* IAO
* RO

---

# Ontology Metadata

## Ontology IRI

```text
http://purl.org/marc-21/ontology
```

## Version IRI

```text
http://purl.org/marc-21/releases/1.0
```

## Namespace Prefix

```text
mbfo:
```

Example:

```text
mbfo:Person
mbfo:Library
mbfo:BibliographicWork
```

---

# Imported Ontologies

## BFO

```text
http://purl.obolibrary.org/obo/bfo.owl
```

## IAO

```text
http://purl.obolibrary.org/obo/iao.owl
```

## RO

```text
http://purl.obolibrary.org/obo/ro.owl
```

---

# Repository Structure

```text
marc-21-bfo/
├── ontology/
│   └── marc21.owl
├── releases/
│   └── 1.0/
│       └── marc21.owl
├── README.md
└── LICENSE
```

---

# Development Methodology

The ontology follows an iterative ontology engineering workflow:

1. Domain Analysis
2. Competency Questions
3. Conceptual Modeling
4. Alignment with BFO
5. OWL Implementation
6. Reasoning and Validation
7. Documentation
8. Publication

---

# FAIR Principles

The ontology is designed to comply with FAIR principles:

* Findable
* Accessible
* Interoperable
* Reusable

Persistent identifiers are provided through PURL resolution.

Source code and ontology files are publicly available through GitHub.

---

# Repository

GitHub Repository: https://github.com/andrew-paes/marc-21-bfo

---

# License

GNU General Public License v2.0 (GPL-2.0)

See LICENSE for details.

---

# Citation

If you use this ontology in academic work, please cite:
* PAES DA SILVA, ANDREW;
* SOARES, M. M.;

MARC21-BFO Ontology: A BFO-Based Ontological Model for Bibliographic Catalogs and MARC 21 Records.
Version 1.0.

---

# Status

Current Status:
```text
Conceptual Modeling and OWL Development
```

Planned future releases:
* Complete OWL axioms
* SHACL validation rules
* MARC field mappings
* FRBR alignment refinements
* Linked Open Data publication
* OBO Foundry compliance assessment