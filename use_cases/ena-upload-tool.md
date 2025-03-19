---
title: ENA Upload Tool
sidebar: use-cases
permalink: /use-cases/ena-upload-tool
custom_repo_url: https://github.com/ELIXIR-Belgium/datahub-test-documentation
custom_repo_branch: datahub-latest-documentation
---

## What is the ENA Upload Tool?

The ENA Upload Tool is a commandline tool developed by [Elixir-Belgium](https://www.elixir-belgium.org/), which can be used to facilitate the submission of your experimental data towards ENA.

The tool supports the following file format for the experimental metadata:

- Excel spreadsheets
- ISA-JSON

You can use the CLI-tool on your own computer or use it on [usegalaxy.be](https://usegalaxy.be/) where a user-friendly GUI will guide you through the process.

The full extend of the documentation on the ENA Upload Tool can be found on the [GitHub page](https://github.com/usegalaxy-eu/ena-upload-cli).

## Step-by-step guide

This guide describes the steps to perform a submission of experimental data and metadata towards ENA. The guide starts from the perspective of a metadata producing platform, which is DataHub in this case, and feeds the metadata together with the data to the ENA Upload Tool.

The usage of the ENA Upload Tool is split in two flows, depending on your personal preference. Follow the [Using the CLI tool](#using-the-cli-tool) guide to use the CLI from the terminal or the [On usegalaxy.be](#on-usegalaxybe) guide to do the test submission through usegalaxy.

Feel free to use your own experimental data and metadata to do the submission or use our public demo experiment on [DataHub Use-case](https://datahub-usecase.elixir-belgium.org/investigations/1) to follow along.

### Exporting your experimental metadata

When exporting the metadata from DataHub to the ISA-JSON format, it is always done from the investigation level.

Steps:

- Go to the investigation level
- Click export ISA
- Save the JSON file on your device

### Start a submission towards ENA

For the actual submission towards ENA, we refer to the '[ENA Data Submission Toolbox](https://rdm.elixir-belgium.org/ena-submission)' article in the RDM Guide, which describes how to use the ENA Upload Tool.
