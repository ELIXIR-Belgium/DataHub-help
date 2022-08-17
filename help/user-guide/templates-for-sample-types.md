---
title: SEEK User Guide - Templates
layout: page
---
 
# Templates
## What are Templates
Templates consist of a set of defined attributes (as columns) needed to create Sample Types, and therefore samples, in experiments (Study, Assay) of a Project in Single Page. Templates act as blueprints that can be shared, reused and applied for creating Sample Types in Studies and Assays, in Single Page.

Conceptually, a Template can be considered as the master copy of a spreadsheet template that you share with your collaborators, so that each collaborator can use his/her own copy of the spreadsheet template to describe samples, by using the same defined attributes/columns.

## Creating Templates
* Select Create in the top navigation bar and choose Template (under Samples section) from the dropdown menu
* Create Template starting from 
  * “Form”: this option is NOT AVAILABLE yet (you will encounter error messages when trying to save the template)
  * “Create template using existing templates”: choose this option to start creating your Template (see below).
* Select “Choose from existing templates”. Note that you will be able to see only the existing templates that are made visible to you (see sharing permission).
  * Filter existing templates
    * Based on repository name
    * If it is a Study or an Assay template
    * If it is organism-specific
  * Choose the resulting template from the dropdown menu
  * Customise the template by
    * Setting attributes as “required”
    * Removing optional attributes
  * Select Apply to create the related Sample Type for the Study or Assay. Note that you will be able to add new attributes to the Sample Type later on in the template creation page.
* Associate Projects and set Sharing permissions
* Add new attributes (if needed). Note that newly added attributes are NOT YET included in the ISA.json export.
* Select Create.

## Template for Sample Types VS Sample Types in Single Page VS Sample Types: what are the differences
Differences between:
* Templates for Sample Types
* Sample Types generated from Templates in Single Page view
* Sample Types

|                                | Template (for Sample Types)                                                                                                  | Sample Type from Template in Single Page                                                                                                                      | Sample Type                                                                                                                                  |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Must belong to project(s)      | Yes                                                                                                                          | Yes, but indirectly via a Study or an Assay                                                                                                                   | Yes                                                                                                                                          |
| Must belong to one Study/Assay | No, not possible                                                                                                             | Yes                                                                                                                                                           | No, not possible                                                                                                                             |
| Has sharing permission         | Yes                                                                                                                          | Not yet. TBD.                                                                                                                                                 | No                                                                                                                                           |
| Created from                   | * Form (NOT YET POSSIBLE)<br> * Existing template                                                                            | * By applying a Template to Design Study/Assay in Single Page                                                                                                 | * Form<br> * Spreadsheet template                                                                                                            |
| Generate                       | Sample Type when applied to Design Study and Assay in Single Page. Many Sample Types can be generated from the same Template | Dynamic Table (Export as CSV) in Single Page                                                                                                                  | Spreadsheet when downloaded (also called template)                                                                                           |
| Reuse of attributes            | Yes. Attributes from a Template can be reused in many different Sample Types                                                 | Yes, the attributes of a Study/Assay Sample Type (created in Single Page) come from one Template                                                              | No. Attributes from a Sample Type are specific for that Sample Type only                                                                     |
| Contain Samples                | No                                                                                                                           | Yes                                                                                                                                                           | Yes                                                                                                                                          |
| Samples batch upload           | No                                                                                                                           | Yes, by pasting samples description using “Paste from Clipboard”                                                                                              | Yes, by uploading a spreadsheet containing samples description that matches an existing Sample Type as data file and then extracting samples |
| Browsing Samples               | No, because Templates don’t contain Samples                                                                                  | Samples (across different Sample Types) can be queried by Template and Template attribute used to generate multiple Sample Types (Export query result as CSV) | Samples can be browsed only within one Sample Type (via “View samples”)                                                                      |
| Exported in ISA.json file      | No, because Templates don’t contain Samples                                                                                  | Yes, possible for experiments (ISA) generated in Single Page, by applying Templates for Study and Assays                                                      | Not possible for experiments (ISA) that have not been created in Single Page                                                                 |



