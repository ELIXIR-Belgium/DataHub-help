---
 title: SEEK User Guide - ISA in Single Page advanced
 layout: page
---

# ISA in Single Page

When using Single Page to organise your Project, you structure your research according to the ISA metadata framework and it can be exported as ISA-JSON. When refering to Investigation, Study and Assay in Single Page we refers to ISA Investigation, ISA Study and ISA Assay.

## ISA Investigation

When desining an ISA Investigation, it will be created within the Project that is visualised in Single Page. You can't assign the ISA Investigation to any other Project during its creation in Single Page.

## ISA Study

An ISA Study is a central unit that must contain the description (metadata) of:

1. *Source(s)* - the subjects or observation units under study (e.g. plants, mouse models, patients, cultured cells, microorganisms).

2. *Protocol* - samples collection protocol, SOP or materials and methods describing the sampling process from Source (e.g. leaves harvesting, biopsy procedure, aliquoting).

3. *Sample(s)* - the physical material which results from the sampling protocol (e.g. leaves, biopsies, aliquotes).

When desining an ISA Study, it will be created within the Investigation that is visualised in Single Page. You can't assign the ISA Study to any other Investigation during its creation in Single Page.

### Example
(image)

## ISA Assay

An ISA Assay*, in Single Page, is in general the application of a protocol (SOP) to inputs that leads to the generation of outputs. Therefore, an ISA Assay must have Inputs, a Protocol and Outputs. In an ISA Assay, every input must have at least one output (or more) and every output (Assay sample) must have at least one input (or more).

1. The inputs can be defined as:
* existing *Sample(s)* created in the Study (e.g. leaves, biopsies, aliquotes). This must be the case for Assays directly performed on the *Sample(s)* of the Study;
* existing outputs of an Assay (Assay samples) that precedes the one you are creating in the same Study.

2. The Protocol can describe:
* an experimental step (e.g. nucleic acids extraction, library construction);
* a data (pre)processing step (e.g. data normalisation).

3. The outputs of an Assay, or ISA Assay samples, are samples that can be:
* physical materials (e.g. nucleic acids extracts, RNA libraries) generated from an experimental step;
* data files (e.g. files containing measurements, rawdata.fastq, processed data, reads.counts.txt).

When desining an ISA Assay, it will be created within the Study that is visualised in Single Page. You can't assign the ISA Assay to any other Study during its creation in Single Page.

**The definition of ISA Assay in Single Page corresponds to one "process" in the ISA metadata framework.*

### Example
(image)

## Stream of ISA Assays
In Single Page, multiple ISA Assays can be interlocked, as one stream of Assays*, if the outputs of an Assay are used as inputs of another Assay, in the same Study.

The outputs of an Assay can be used as inputs **only by one, and only one, other Assay** in the same Study. In other words, the outputs of an Assay cannot be used as inputs in multiple Assays, in the same Study.

**The definition of a Stream of ISA Assays in Single Page corresponds to one "assay" in the ISA metadata framework.*

### Example
(image)


# Templates

Templates act as blueprints to create Sample types within ISA Studies and ISA Assays. The same Template can be (re)used multiple times to create Sample Types in different ISA Studies or ISA Assays.

Single Page, <!--what about in default view? do we allow use of template w/o ISA tag there? --> the use of Templates to design ISA Studies and ISA Assays  is mandatory <!--or there is an error--> since they are needed for the export of ISA-JSON.

## Templates providers

Templates can be [provided by FAIRDOM-SEEK administrator](templates-for-admin.html) or created by Project members. <!--create = create vs submit. specify later everywhere-->

* FAIRDOM-SEEK administrator
  * are not associated to any specific Programme or Project
  * are available to all Projects

* Project members
  * must be associated (created within) at least one or more Project <!--see difference between associated VS shared with-->
  * must have specific sharing permission settings, as defined by the their creators
  <!-- * currently not working if made from scratch or if changes are made starting from the administrators' ones>

## Template characteristics

A Template must have the following characteristics.
1. Level or type: a Template must be an
    * ISA Study Template for Study *Sources* or 
    * ISA Study Template for Study *Samples* or <!-- I don't remember how this distinction happens-->
    * ISA Assay Template for Assay samples

2. Repository name or SEEK Project <!--We might need to introduce more granularity here in case Project members create their own vesrion of a repository template, starting from the instance one-->
    * EBI repository
    * SEEK Project

3. Organism

### Example
(image)


# Sample Types in Single Page

In Single Page, a Sample Type is an instance of one Template. Sample Types are created during the design of ISA Studies and ISA Assays, when existing Templates are applied. 
Therefore, each Sample Type is an instance of a Template associated with an ISA Study or an ISA Assay. 

Sample Types derived from Template are needed to create and contain different types of samples: Study Sources, Study Samples and Assay samples.

### Example
(image)


# Samples in Single Page

In Single Page, samples must be created within a Sample Type, derived from a Template, associated with ISA Studies or ISA Assays. 

The "level or type" of the Template applied to generate a Sample Type within an ISA Study or ISA Assay determines the type of samples that will be created. Specifically, 
* ISA Study Template for *Sources* creates Sources
* ISA Study Template for *Samples* creates Samples
* ISA Assay Template for Assay samples creates assay samples

## Types of samples in Single Page

Study Source(s)
* Study Sources must be created within an ISA Study, using a Tempate level "Study Source".
* Each Study Source must be the input of at least one Study Sample (or more) in the same ISA Study.

Study Sample(s)
* Study Samples must be created within an ISA Study, using a Tempate level "Study Sample".
* Study Samples must be the outputs of a sampling protocol applied to ISA Study Sources, in the same Study.
* Each Study Sample must be the output of at least one Source (or more), in the same ISA Study.

Assay sample(s)
* Assay samples must be created within an ISA Assay, using a Tempate level "Assay".
* Assay samples must be the outputs of a protocol applied to the inputs of the Assay.
* Each Assay Sample must have at least one input (or more). Inputs can be: 
  * Study Samples in the same ISA Study;
  * assay samples from one preceding Assay, in the same Stream of ISA Assays.

### Example
(image)

## Browsing samples by templates
[Browsing samples by templates](browsing.html#browsing-samples-by-templates)

# ISA JSON export
## [Export experiments from Single Page as ISA-JSON](exporting-experiments-from-single-page.html)

