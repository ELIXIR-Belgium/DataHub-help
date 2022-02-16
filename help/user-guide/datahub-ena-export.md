---
title: SEEK User Guide - ENA export
layout: page
---

# ENA Export

The ENA export button triggers the export of tables in the TSV file format containing relevant information for the submission of raw nucleotide sequencing data to the European Nucleotide Archive ([ENA](https://www.ebi.ac.uk/ena/browser/home)).

DataHub offers 4 Sample Types tailored for capturing the necessary metadata for submission of raw nucleotide sequencing data to ENA. These serve as templates and ensure that required and useful information for the final submission of data and metadata to the repository is are recorded. Each Sample Type corresponds to one of the necessary input tables for the [ENA-upload-cli](https://github.com/usegalaxy-eu/ena-upload-cli) tool. The Sample Types follow the [ENA Metadata Model](https://ena-docs.readthedocs.io/en/latest/submit/general-guide/metadata.html) and are:
* ENA_study
* ENA_sample
* ENA_experiment
* ENA_run

Information is added as Samples to each Sample Type. For more information, see [Creating a Sample](create-sample.html). Examples for each Sample Type can be found in the [ENA submission example Project](https://datahub.test.elixir-belgium.org/projects/2).

Step by step guide:
1. Select Create and then Sample in the drop down menu.

   ![datahub menu create sample](/images/user-guide/datahub-test-create-sample.png){:.screenshot}

2. Under Other Projects, select the "ENA submission example" Project to display only the 4 ENA export related Sample Types.

   ![datahub ENA sample types](/images/user-guide/datahub-test-ENA-sample-types.png){:.screenshot}

3. Identify the Sample Type you wish to use and select New Sample or New batch submission, depending on the number of Samples you wish to create.

4. Add the information requested in each attribute field presented. An explanation of each attribute for the 4 Sample Types is provided at the end of this page.

   ![datahub ENA_study sample example](/images/user-guide/datahub-test-ENA-sample-ENA_study.png){:.screenshot}

5. After adding all the required information in all the 4 Sample Types, navigate to your Project’s page and click on the ENA export button.
   * Independent tables in TSV format will be exported for all the ENA related Sample Types.
   * Metadata from other Sample Types is not included in the export.
   * Only Samples pertaining to that project, and that you have permission to access, are included in the resulting files.

   ![datahub ENA export](/images/user-guide/datahub-test-ENA-export-button.png){:.screenshot}

6. The resulting tables are ready for submission to ENA using the [ENA-upload-cli](https://github.com/usegalaxy-eu/ena-upload-cli) tool.

Note: Pressing the ENA export button will always generate 4 tables. If no Samples in the Project belong to the Sample Types mentioned, the tables are exported empty.

Instructions on how to use the ENA-upload-cli tool can be found [here](https://github.com/usegalaxy-eu/ena-upload-cli).This tool is used to submit the tables exported from DataHub and the corresponding data files to ENA. The tool provides a receipt file upon successful submission. The tool will also provide you with updated versions of each table. These contain an updated status attribute, and information added by ENA, such as accession numbers and submission date.

## Explanation for the attributes of each Sample Type:
Note that only Attributes with values are submitted to ENA by the ENA-upload-cli tool. Attributes that are empty or contain “NA” or “na” (for “not applicable”) are not submitted.

### ENA_study:
* **alias**: Unique identifier for a study. This is used to link experiments to the study.
* **status**: Allows the ENA-upload-cli tool to filter for Samples that match the action argument upon submission. Please see note at the end of page. 
* **accession**: Attribute updated by ENA-upload-cli during submission. Please leave this attribute blank.
* **title**: Title of the study as it would be used in a publication.
* **study_type**: A controlled vocabulary for expressing the overall purpose of the study.
* **study_abstract**: Briefly describes the goals, purpose, and scope of the Study.
* **pubmed_id**: Provides PubMed IDs of publications you want ENA to associate with the study. Only integers are accepted, please remove “PMID: ” from the identifier.
* **submission_date**: Attribute updated by ENA-upload-cli during submission. Please leave this attribute blank.

### ENA_sample:
This Sample Type is based on ENA’s sample checklist [ERC000011](https://www.ebi.ac.uk/ena/browser/view/ERC000011). It contains a variety of optional attributes and researchers can choose the most appropriate ones for their field. These optional attributes are not described below. Be aware that at least one of the optional attributes must be used.
* **alias**: Unique identifier for each sample. This is used to link experiments to the samples.
* **status**: Allows the ENA-upload-cli tool to filter for Samples that match the action argument upon submission. Please see note at the end of page.
* **accession**: Attribute updated by ENA-upload-cli during submission. Please leave this attribute blank.
* **title**: Short text that can be used to call out sample records in search results or in displays in ENA.
* **Scientific_name**: Attribute updated by ENA during submission, based on the taxon_id attribute. Please leave this attribute blank.
* **taxon_id**: Unique taxonomy identification number. This attribute is used to fetch the correct value for the scientific_name attribute. Identification numbers can be found using the [NCBI's Taxonomy Browser](https://www.ncbi.nlm.nih.gov/Taxonomy/Browser/wwwtax.cgi) or [EBI's OLS page for NCBItaxon page](https://www.ebi.ac.uk/ols/ontologies/ncbitaxon). For example, 4932 for baker's yeast. 
* **sample_description**: Free-form text describing the sample, its origin, and its method of isolation.
* **submission_date**: Attribute updated by ENA-upload-cli during submission. Please leave this attribute blank.

### ENA_experiment:
* **alias**: Unique identifier for each experiment. This is used to link runs to experiments.
* **status**: Allows the ENA-upload-cli tool to filter for Samples that match the action argument upon submission. Please see note at the end of page.
* **accession**: Attribute updated by ENA-upload-cli during submission. Please leave this attribute blank.
* **title**: Short text that can be used to call out experiment records in searches or in displays. This element is technically optional but should be used for all new records.
* **study_alias**: From “alias” attribute in ENA_study Sample Type. Used to link experiments with studies.
* **sample_alias**: From “alias” attribute in ENA_sample Sample Type. Used to link experiments with samples.
* **design_description**: Goal and setup of the individual library including how the library was constructed.
* **library_name**: The submitter's name for this library.
* **library_strategy**: Sequencing technique intended for this library.
* **library_source**: Specifies the type of source material that is being sequenced.
* **library_selection**: Method used to enrich the target in the sequence library preparation.
* **library_layout**: Specifies whether to expect single or paired configuration of reads. In the case of paired reads, information about the relative distance and orientation is specified in the insert_size attribute.
* **insert_size**: Insert size for paired reads.
* **library_construction_protocol**: Free form text describing the protocol by which the sequencing library was constructed.
* **platform**: The sequencing platform and platform-specific runtime parameters.
* **instrument_model**: Model of the sequencing instrument.
* **submission_date**: Attribute updated by ENA-upload-cli during submission. Please leave this attribute blank.

### ENA_run:
* **alias**: Unique identifier for each run.
* **status**: Allows the ENA-upload-cli tool to filter for Samples that match the action argument upon submission. Please see note at the end of page.
* **accession**: Attribute updated by ENA-upload-cli during submission. Please leave this attribute blank.
* **experiment_alias**: From “alias” attribute in ENA_experiment Sample Type. Used to link runs with experiments.
* **file_name**: The name of a run data file. The name has to be an exact match to the name of the data file being submitted to ENA, including the file extension.
* **file_format**: The run data file model. For further information file formats and how to prepare data files for submission, check ENA’s [Accepted Read Data Formats](https://ena-docs.readthedocs.io/en/latest/submit/fileprep/reads.html#accepted-read-data-formats).
* **file_checksum**: Attribute updated by ENA-upload-cli during submission. Please leave this attribute blank.
* **submission_date**: Attribute updated by ENA-upload-cli during submission. Please leave this attribute blank.

### Note on the status attribute:
The “status” attribute is used by the ENA-upload-cli tool to filter rows of the input TSV tables generated by the ENA export feature. During a submission, a “status” value that does not match the “--action” argument given to the ENA-upload-cli will lead to the exclusion of that row for that submission.
Upon a successful submission, the updated tables generated by the ENA-upload-cli will contain a corresponding updated “status” value. This way, it is easier to keep track of the last action taken for that Sample. The possible values for the “status” attribute are:
* add: add an object to ENA
* added: updated value for an object that was added to ENA
* modify: modify an object in ENA
* modified: updated value for an object that was modified in ENA
* cancel: cancel a private object and its dependent objects
* cancelled: updated value for a private object, and its dependents, that was cancelled
* release: release a private object immediately to the public
* released: updated value for a private object that was immediately released to the public
