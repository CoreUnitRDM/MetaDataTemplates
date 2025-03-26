# FAIR RDM Metadata Templates for Research Consortia

This repository contains Python code that generates Excel workbooks designed as metadata templates for research consortia such as DECIDE, GvHGvL, and others. These templates have been developed in association with Würzburg and the Core Unit RDM (cRDM, [https://www.med.uni-wuerzburg.de/fdm/](https://www.med.uni-wuerzburg.de/fdm/)).

## Overview

The code leverages [openpyxl](https://openpyxl.readthedocs.io/) to create an Excel workbook that contains two key sheets:

- **MetaDataTemplate:**  
  A structured template for entering study metadata. This sheet contains headers such as Category, Key, Value, Example_Value, Description, Controlled_Vocabulary/Value-Restrictions, and Resource_Link(s). Drop-down validations are applied to key fields using controlled vocabulary lists.

- **Database:**  
  A dedicated sheet that stores controlled vocabulary values for various fields (e.g., Organism, Tissue, Cell_Type, Strain Identifier, Library Preparation Method, Sequencing Platform, etc.). Named ranges are created for these values, which are then referenced in the MetaDataTemplate sheet to ensure consistency.

These metadata templates are a cornerstone of FAIR Research Data Management (RDM) as they guarantee that metadata is standardized and attached to the project or data folder. This supports data reuse and contributes to the research data lifecycle by promoting the findability, accessibility, interoperability, and reusability of research data.

## Key Features

- **Controlled Vocabulary:**  
  All critical fields use controlled vocabulary. For example, reference genomes, sequencing platforms, and gene annotations are populated with commonly used values.

- **Data Validations:**  
  Drop-down validations are applied to key fields in the MetaDataTemplate, ensuring that users select values only from the predefined lists.

- **Styling and Formatting:**  
  Both the MetaDataTemplate and Database sheets are styled with custom fonts, fills, and column widths for improved readability.

- **Extensible and Reusable:**  
  The templates are designed to be easily adapted to different research consortia. The controlled vocabulary values can be extended or modified as needed.

## Prerequisites

- Python 3.x
- [openpyxl](https://pypi.org/project/openpyxl/)

You can install openpyxl via pip:

```bash
pip install openpyxl

