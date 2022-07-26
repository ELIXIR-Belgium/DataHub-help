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
* Define Sample Type for Sample
  * Choose a Template to create a Sample Type to describe your Samples by selecting Existing Templates button (see difference between Template and Sample Type)
  * Filter existing Templates and choose one from the drop down menu. Before selecting “Apply”, use the Attributes table to:
    * Set attributes as “Required” or not
    * Remove not required attributes
  * Select “Add new attributes” at the bottom of the page if you want to add new attributes of your choice to your Sample Type for Sample in the Assay. Attributes in the Sample Type for Sample will be the columns in a table that require information about
    * The method, the protocol and its parameters applied to the Assay to generate the Assay’s outputs
    * Any relevant characteristics of the Assay’s outputs, from sample’s amount and quality to storage of each physical tube in a laboratory or of each digital data file in a storage.
* Select one SOP (Protocol), which is already registered in SEEK, describing the used  protocol in the Assay. See how to create an SOP in SEEK.
