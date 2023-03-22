---
title: SEEK User Guide - Create Sample in Single Page
layout: page
---

# Viewing samples in Single Page
In Single Page, all kind of [samples](isa-single-page-advanced.html#samples-in-single-page) created via Single Page are grouped in tables, corresponding to the sample types defined during the ISA Study and ISA Assay design. Tables can be accessed via the tree view on the left sidebar or via the design tab for Study and Assay.

## Sources table and Samples table
Sources table and Samples table are interactive tables (dynamic tables) that allow samples creation and editing. 
* Studies contain both Sources table and Samples table.
* Assays contains only Samples table.

They can both be accessed via tree view (image 1) and the design tab (image 2a/b)

## samples
From tree view on the left sidebar, Study sources, Study Samples and Assay samples can also be viewed in a searchable table via selecting samples.

(image)

## Experiment overview
Experiment overview table shows an overview of all Sources and Samples in a searchable table.
* In Study, Experiment overview shows Study Sources and Study Samples.
* In Assay, Experiment overview shows Study Study Samples and Assay samples, up until that experimental step.

Experiment overview table can be accessed via tree view (image 1) and the design tab (image 2a/b).

# Create Study Sources 
* Select the Study in the tree view and then select Sources table item 
(image)

* Or Select the Study in the tree view and then select the Study design tab at the center of the page, which shows the Sources table tab.

Via dynamic table, you can create Sources in two/3? ways.

## Via the Add row button. 
1. Select the Add row button at the bottom of the page to start. (image) One row corresponds to one Source.
2. Make sure to fill in all the mandatory columns and then select Save. (image) (link to more info about sample type attributes to explain "title", "required" etc)
* Note that the Source name column will define the name of each Source.
3. Click on Save. For each row that gets saved, a single Study Source is created. (image)
  

## Via the Paste From Clipboard button
1. Download or export the table
2. Fill in the table (in excel) and copy the content
* somenthing about ignoring or how to use SEEK ID? here or link to?
3. Use the Paste From Clipboard button at the bottom of the page to fill in the table. 
4. Select Save. For each row that gets saved, a single Source is created.

## Via upload of spreadsheet ? (is it still via dynamic table?)

# Create Study Samples 
* Select the Study in the tree view and then select Samples table item 
(image)

* Or Select the Study in the tree view, then select the Study design tab at the center of the page, and then select Samples table tab.

Via dynamic table, you can create Study Samples in two/3? ways.

## Via the Add row button. 
1. Select the Add row button at the bottom of the page to start. (image). One row corresponds to one Sample.
2. Select the input Source(s) for the Sample your are creating in the "Input (Source name)" column. (more explaination in attribute type? or in [isa overview](isa-single-page-advanced)?)
3. Make sure to fill in all the mandatory columns. (image) (link to more info about sample type attributes to explain "title", "required" etc)
* Note that the Source name column will define the name of each Sample and the corresponding column will be highlighted in light blue.
4. Click on Save. For each row that gets saved, a single Study Sample is created. (image)
  

## Via the Paste From Clipboard button
1. Download or export the table
2. Fill in the table (in excel) and copy the content
* somenthing about ignoring or how to use SEEK ID? here or link to?
3. Use the Paste From Clipboard button at the bottom of the page to fill in the table. 
* Note that the Source name column will define the name of each Sample and the corresponding column will be highlighted in light blue.
4. Select Save. For each row that gets saved, a single Source is created.

## Via upload of spreadsheet ? (is it still via dynamic table?)

# Create samples in a first Assay 
<!--differences with second Assay?-->
* Select the Assay in the tree view and then select Samples table item 
(image)

* Or Select the Assay in the tree view, then select the Assay design tab at the center of the page, and then select Samples table tab.

Via dynamic table, you can create Assay Samples in two/3? ways.

## Via the Add row button. 
1. Select the Add row button at the bottom of the page to start. (image). One row corresponds to one sample.
2. Select the input for the sample your are creating in the "Input" column. (more explaination in attribute type? or in [isa overview](isa-single-page-advanced)?)
* first assay (consecutive after the Study): the input must be Study Sample(s); Input column is "Input (Sample name)"
* not the first assay (consecutive after another Assay): the input must be Assay sample(s); Input column is "Input (Sample name)"
3. Make sure to fill in all the mandatory columns. (image) (link to more info about sample type attributes to explain "title", "required" etc)
* Note that the sample name column will define the name of each sample and the corresponding column will be highlighted in light blue.
4. Click on Save. For each row that gets saved, a single Assay sample is created. (image)
  

## Via the Paste From Clipboard button
1. Download or export the table
2. Fill in the table (in excel) and copy the content
* somenthing about ignoring or how to use SEEK ID? here or link to?
3. Use the Paste From Clipboard button at the bottom of the page to fill in the table. 
* Note that the sample name column will define the name of each sample and the corresponding column will be highlighted in light blue.
4. Select Save. For each row that gets saved, a single Assay sample is created.

## Via upload of spreadsheet ? (is it still via dynamic table?)