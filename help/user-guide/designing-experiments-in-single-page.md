---
title: SEEK User Guide - Designing experiments in Single Page
layout: page
---

# Designing experiments in Single Page
Single page guides you to organise your experiments according to the [ISA metadata framework](https://isa-specs.readthedocs.io/en/latest/isamodel.html). The framework requires the description (metadata) of different types of samples (Study Sources, Study Samples and Assay samples) according to provided but customisable Templates and the linking of applied Protocols. Follow the link for an overview about the components of [ISA in Single Page](isa-single-page-advanced.html).

## 1. Creating an ISA Investigation in Single Page
Wwithin the Project in Single Page, select Create <!--it should be Design--> Investigation button at the top right corner of the single page view, fill in the shown form and select Create button.

## 2. Creating an ISA Study in Single Page
To start designing a Study within the Investigation in Single Page, select the Investigation level in the tree view and then select the Design Study button at the top right corner of the single page view. 
(image)

Start filling in the shown form as explained below.

(Link to general attributes here? like, Title, etc)

## 2.1 Design a Sample Type for Study Sources
In Single Page, a [Sample Type](isa-single-page-advanced.html#sample-types-in-single-page) is an instance of a [Template](isa-single-page-advanced.html#templates) to describe and create [samples](isa-single-page-advanced.html#samples-in-single-page). Attributes for Source Sample Type will be the columns in a table that require information about
* Biological material and its origin or provenance
* Environmental and/or experimental conditions of the Sources in the Study
* Experimental groups of the Sources
* Experimental factor(s), confounding variables, covariates, events, comments etc
* Any other relevant information about the Sources in the Study

(see example)

### 2.1.1 Choose a Template

* Choose from an existing Template to create a Sample Type to describe your Sources (or observation units) by selecting Existing Templates button <!--(see difference between Template and Sample Type?)-->

(image)

* Filter existing Templates based on:
  * the repository that will store metadata about your Study Sources (e.g. ENA, ArrayExpress or your institutional repository). Other if it is institutional repo? To be tested <!--BioSamples in the future?-->
  * the type of samples you are describing: Study. Note: make sure that the template has ‘source’ in its name. <!--Study should be the only possible selection and well as Source. To be discussed and developed-->
  * organism

* Choose a template from the resulting dropdown menu and use the Attributes table to:
  * Set attributes as “Required” or not
  * Remove not required attributes
Then select "Apply"

(image)

### 2.1.2 Customise and create the Study Source Sample Type 

* If you want to add new attributes of your choice to your Source Sample Type for the Study, select “Add new attributes” at the bottom of the page.

* Give a Title <!--TBD--> and a description to your Sample Type.

## 2.2 Link the sampling Protocol 
Select one Protocol, which is already registered in SEEK, describing the used method or procedure for collecting Samples from Sources in your Study (Samples collection protocol). See how to [create an SOP](adding-assets.html) in SEEK.

## 2.3 Design a Sample Type for Study Sample

In Single Page, a [Sample Type](isa-single-page-advanced.html#sample-types-in-single-page) is an instance of a [Template](isa-single-page-advanced.html#templates) to describe and create [samples](isa-single-page-advanced.html#samples-in-single-page). Attributes in the Sample Type for Sample will be the columns in a table that require information about
* Collection method or parameters used in the sample collection protocol of the physical Sample from the Source, such as collection date, experimentalist etc.
* Any relevant characteristics of the Sample in the Study, from anatomy and developmental stage to storage of each physical tube in a laboratory.

(see example)

### 2.3.1 Choose a Template

* Choose from an existing Template to create a Sample Type to describe your Sample by selecting Existing Templates button <!--(see difference between Template and Sample Type?)-->

(image)

* Filter existing Templates based on:
  * the repository that will store metadata about your Study Sample (e.g. ENA, ArrayExpress or your institutional repository). Other if it is institutional repo? To be tested <!--BioSamples in the future?-->
  * the type of samples you are describing: Study. Note: make sure that the template has ‘sample’ in its name. <!--Study should be the only possible selection and well as Source. To be discussed and developed-->
  * organism

* Choose a template from the resulting dropdown menu and use the Attributes table to:
  * Set attributes as “Required” or not
  * Remove not required attributes

* Then select "Apply"

(image)

### 2.3.2 Customise and create the Sample Type for Study Sample

* If you want to add new attributes of your choice to your Sample Type for Study Sample, select “Add new attributes” at the bottom of the page.

* Give a Title <!--TBD--> and a description to your Sample Type.

## 2.4 Visualise ISA Study 
Upon creation, the newly designed ISA Study will appear in the tree view on the left sidebar.

Follow the link to know more about [ISA visualisation in Single Page](viewing-project-in-single-page.html) or about [viewing samples in Single Page](create-sample-single-page-advanced.html#viewing-samples-in-single-page).

## 3. Adding Sources to ISA Study
After you have designed the Sample Types (tables) for your Sources, you can then start by first creating and describing your Study Sources according the designed tables.

Follow the link to know how to [create samples](create-sample-single-page-advanced.html) in Single Page, including [Study Sources](create-sample-single-page-advanced.html#create-study-sources).

## 4. Adding Samples to ISA Study

Follow the link to know how to [create samples](create-sample-single-page-advanced.html) in Single Page, including [Study Samples](create-sample-single-page-advanced.html#create-study-samples).

## 5. Creating a first ISA Assay in Single Page
<!--differences with second Assay?-->
To start designing an ISA Assay within a Study in Single Page, select the Study level in the treeview and then select the Design Assay button at the top right corner of the Single Page view.
(image)

Start filling in the shown form as explained below.

(Link to general attributes here? like, Title, etc

## 5.1 Link a Protocol to the Assay
Select one Protocol, which is already registered in SEEK, describing the used method or procedure applied to Study Samples to perform the Assay. See how to [create an SOP](adding-assets.html) in SEEK.

## 5.2 Design a Sample Type for Assay samples
In Single Page, a [Sample Type](isa-single-page-advanced.html#sample-types-in-single-page) is an instance of a [Template](isa-single-page-advanced.html#templates) to describe and create [samples](isa-single-page-advanced.html#samples-in-single-page). Attributes for Assay Sample Type will be the columns in a table that require information about
* the method, the protocol and its parameters applied to the Assay to generate the Assay’s outputs
* any relevant characteristics of the Assay’s outputs, from sample’s amount and quality to storage of each physical tube in a laboratory or of each digital data file in a file storage system.

(see example)

### 5.2.1 Choose a Template

* Choose from an existing Template to create a Sample Type to describe your samples by selecting Existing Templates button <!--(see difference between Template and Sample Type?)-->

(image)

* Filter existing Templates based on:
  * the repository that will store metadata about your Study Sample (e.g. ENA, ArrayExpress or your institutional repository). Other if it is institutional repo? To be tested <!--BioSamples in the future?-->
  * the type of samples you are describing: Assay. <!--Assay should be the only possible selection. Other is because we thought to provide the same features even for "ISA" not compliant to ISA specifications. Still valid argument?-->
  * organism

* Choose a template from the resulting dropdown menu and use the Attributes table to:
  * Set attributes as “Required” or not
  * Remove not required attributes

* Then select "Apply"

(image)

### 5.2.2 Customise and create the Sample Type for Assay samples

* If you want to add new attributes of your choice to your Sample Type for Assay samples, select “Add new attributes” at the bottom of the page.

* Give a Title <!--TBD--> and a description to your Sample Type.

## 5.3 Visualise ISA Assay 
Upon creation, the newly designed ISA Assay will appear in the tree view on the left sidebar.

Follow the link to know more about [ISA visualisation in Single Page](viewing-project-in-single-page.html) or about [viewing samples in Single Page](create-sample-single-page-advanced.html#viewing-samples-in-single-page).
    
## 6. Adding samples to the first ISA Assay <!--differences with second Assay?-->

Follow the link to know how to [create samples](create-sample-single-page-advanced.html) in Single Page, including [Assay samples](create-sample-single-page-advanced.html#create-samples-in-a-first-assay).
