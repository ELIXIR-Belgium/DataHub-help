---
title: SEEK User Guide - Designing experiments in Single Page
layout: page
---

# Designing experiments in Single Page
A Project and its content can be visualised in a single page view by clicking the Single Page button on the top of the Project page.

In Single Page, you can design the experiments for your Project, describe and create Samples and export the information as table (spreadsheet in CSV format) and ISA-JSON format.

## Creating an Investigation in Single Page
The Investigation is a high level concept that links related Studies. An Investigation must belong to only one Project and multiple Investigations can belong to the same Project.

To generate an Investigation within the Project in Single Page, select Create Investigation button at the top right corner of the single page view, fill in the shown form and select Create button.

## Creating a Study in Single Page
A Study is a central unit containing information about the subjects or observation units under study (Source, e.g., plants, mouse models, patients, cultured cells, microorganisms, etc), the Sample collection protocol and the resulting physical Samples (e.g., organism parts as leaves or biopsies, sub-cultures etc). A Study must belong to only one Investigation and multiple Studies can belong to the same Investigation.

To generate a Study within the Investigation in Single Page, select Design Study from the button at the top right corner of the single page view, fill in the shown form and select Create button.

A Study creation via Design Study button in Single Page view requires the following conditions:
* Define Sample Type for Source (or observation unit)
  * Choose a Template to create a Sample Type to describe your Sources (or observation units) by selecting Existing Templates button (see difference between Template and Sample Type)
  * Filter existing Templates and choose one from the drop down menu. Before selecting “Apply”, use the Attributes table to:
    * Set attributes as “Required” or not
    * Remove not required attributes
  * Select “Add new attributes” at the bottom of the page if you want to add new attributes of your choice to your Source Sample Type for the Study. Attributes for Source Sample Type will be the columns in a table that require information about
    * Biological material and its origin or provenance
    * Environmental and/or experimental conditions of the Sources in the Study
    * Experimental groups of the Sources
    * Experimental factor(s), confounding variables, covariates, events, comments etc
    * Any other relevant information about the Sources in the Study
* Select one SOP (Protocol), which is already registered in SEEK, describing the used method or procedure for collecting samples in your study (Samples collection protocol). See how to create an SOP in SEEK.
* Define Sample Type for Sample
  * Choose a Template to create a Sample Type to describe your physical Samples by selecting Existing Templates button
  * Filter existing Templates and choose one from the drop down menu. Before selecting “Apply”, use the Attributes table to:
    * Set attributes as “Required” or not
    * Remove not required attributes
  * Select “Add new attributes” at the bottom of the page if you want to add new attributes of your choice to your Sample Type for Samples in the Study. Attributes in the Sample Type for Sample will be the columns in a table that require information about
    * Collection method or parameters used in the sample collection protocol of the physical Sample from the Source, such as collection date, experimentalist etc
    * Any relevant characteristics of the Sample in the Study, from anatomy and developmental stage to storage of each physical tube in a laboratory.

## Creating an Assay in Single Page
An Assay is an experimental step or data (pre)processing step or in general the application of a protocol (SOP) to:
* Some input material (e.g. a Sample) to produce some physical output (e.g. an extract of nucleic acids)
* Some input material (e.g. a RNA library) to produce some measurements or data in the form of data files (e.g. a sequencing file in .fastq)
* Some measurements or data (such as raw data file) to produce (pre)processed measurements/data (e.g. normalized data file, reads.counts.txt).

An Assay must belong to only one Study and multiple Assays can belong to the same Study. The Study Samples must be the inputs of at least one Assay in the same Study. Multiple Assays can be interlocked if the outputs of an Assay are used as inputs of another Assay in the same Study. 
*Note*: the outputs of an Assay can be used as inputs only by one and only one other Assay in the same Study. In other words, the outputs of an Assay cannot be used in multiple Assays as inputs.

To generate an Assay within the Study in Single Page, select Design Assy from the button at the top right corner of the single page view, fill in the shown form and select Create button.

An Assay creation via Design Assay button in Single Page view requires the following conditions:
* Select one SOP (Protocol), which is already registered in SEEK, describing the used  protocol in the Assay. See how to create an SOP in SEEK.
* Define Sample Type for Sample
  * Choose a Template to create a Sample Type to describe your Samples by selecting Existing Templates button (see difference between Template and Sample Type)
  * Filter existing Templates and choose one from the drop down menu. Before selecting “Apply”, use the Attributes table to:
    * Set attributes as “Required” or not
    * Remove not required attributes
  * Select “Add new attributes” at the bottom of the page if you want to add new attributes of your choice to your Sample Type for Sample in the Assay. Attributes in the Sample Type for Sample will be the columns in a table that require information about
    * The method, the protocol and its parameters applied to the Assay to generate the Assay’s outputs
    * Any relevant characteristics of the Assay’s outputs, from sample’s amount and quality to storage of each physical tube in a laboratory or of each digital data file in a storage.

## Creating samples in Single Page
In Single Page, SEEK samples can be
* “Sources”: Sources must belong to one Study.
* “Samples” in a Study: Samples in Study must derive from the Sources and must belong to the same Study.
* “Samples” in an Assay: Samples in Assay must derive from the Samples of the Study or of another Assay, and must belong to an Assay related to the same Study.

Therefore, creating SEEK samples in Single Page need the following prerequisites:
* The Project must have Investigation with at least one Study in order to create Sources and Samples in Study.
* The Study must have at least one Assay in order to create Samples in Assay.

### Creating Sources in Study
* In Project Single Page tree view (on the left side), select the Investigation.
* Create a Study by using the Design Study button at the top right corner of the Investigation page. See Creating a Study in Single Page. 
* Select the Study in the tree view 
  * then the Study design tab at the center of the page. Go to the Sources table tab, which shows the headers (columns) of your Source Sample Type. 
  * Or alternatively, select Sources table item under Study in the tree view.
* You can create Sources in two ways:
  * Select the Add row button at the bottom of the page to start. Make sure to fill in all the mandatory columns and then select Save. For each row that gets saved, a single Source is created.
  * Use the Paste From Clipboard button at the bottom of the page to fill in the table, if you have the information (metadata) elsewhere in a matching spreadsheet. For each row that gets saved, a single Source is created.
* Note that:
  * The Source name column will define the name of each source.
  
### Creating Samples in Study
* In Project Single Page tree view (on the left side), select Study in the tree view
  * then the Study design tab at the center of the page. Go to the Samples table tab, which shows the headers (columns) of your Sample Type for Samples in Study. 
  * Or alternatively, select Samples table item under Study in the tree view.
* You can create Samples in the Study in two ways:
  * Select the Add row button at the bottom of the page to start. Make sure to fill in all the mandatory columns and then select Save. For each row that gets saved, a single Samples is created in the Study.
  * Use the Paste From Clipboard button at the bottom of the page to fill in the table, if you have the information (metadata) elsewhere in a matching spreadsheet. For each row that gets saved, a single Sample is created in the Study.
* Note that:
  * The input for this Sample Type must be a Source name as defined in the Sources table. Input cannot be Pasted From Clipboard.
  * The name of the output for this Sample Type or the name of the Samples in this Study will be defined by the column highlighted in light blue.
  
### Creating Samples in Assay
* In Project Single Page tree view (on the left side), select Assay in the tree view, then the Assay design tab at the center of the page. Go to the Samples table tab, which shows the headers (columns) of your Sample Type for Samples in Assay.
* You can create Samples in the Assys in two ways:
  * Select the Add row button at the bottom of the page to start. Make sure to fill in all the mandatory columns and then select Save. For each row that gets saved, a single Samples is created in the Assay.
  * Use the Paste From Clipboard button at the bottom of the page to fill in the table, if you have the information (metadata) elsewhere in a matching spreadsheet. For each row that gets saved, a single Sample is created in the Assay.
* Note that:
  * The input for this Sample Type must be a Sample of the Study or of the previous Assay as defined in the Samples table in Study or in Assay. Input cannot be Pasted From Clipboard.
  * The name of the output for this Sample Type or the name of the Samples in this Assay will be defined by the column highlighted in light blue.
