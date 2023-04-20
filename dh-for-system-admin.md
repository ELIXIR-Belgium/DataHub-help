---
layout: page
title: For System Admin
---

# Simplified view of the model of DataHub database
Some of the most relevant database tables in DataHub model: [partial view](https://dbdiagram.io/d/627d0a687f945876b6082659).

# How to deploy FAIRDOM-SEEK as DataHub

As system administrator, you have access to the Server admin panel. You can go to the Server admin panel by selecting your Name/account at the top right corner and selecting "Server admin" from the dropdown menu.

The following configuration settings must be applied the Server admin page.

## Enable/disable features

### SEEK services

All seetings enabled, except for
* Omniauth enabled
* FAIR Signposting Enabled

### SEEK features

Do not select 

* Internal help enabled and provide the Help URL

### Resource Type

All settings enabled, except for
* Programmes open for Projects enabled
* Workflows enabled

### Integrations

All settings disabled, except for
* Single page enabled
  * Advanced features enabled
* Sample type Template enabled


## Site branding
* Name: DataHub
* Link to: https://datahub.elixir-belgium.org/
* Issue tracker link: <!--https://fair-dom.org/issues-->?
* Instance administrator name: ELIXIR Belgium
* Instance administrator link: https://www.elixir-belgium.org/
* Header logo image enabled with DataHub logo (link to JPEG or PNG file)
* Header image alternative title: DataHub
* Enable
  * Terms and Conditions enabled (link to file?)
  * Privacy policy enabled (link to file?)
* Enable
  * "About" the instance enabled
  * "About" the instance administrator enabled

## Settings

### General settings

Session store timeout (minute): 60

All disabled, except for
* Cache remote files
  * Maximum file size (bytes): 20971520
  * Hard maximum file size (bytes): 104857600

### Policy and license settings

Settings For Default Permissions
* Default permissions option for all visitors, including those without a login: No access
* Default permissions option for members of associated Projects: View summary and get contents

Permission Limits: maximum permission option for all visitors, including those without a login
* View summary and get contents

Default License: the default license to use when one is not specified by a Projects
  * Creative Commons Attribution 4.0

Recommended data licenses: the licenses to recommend when data, such as a Data file or Document, is registered
* CC0 1.0
* Creative Commons Attribution 4.0
* Creative Commons Attribution Share-Alike 4.0
* Creative Commons Attribution-NonCommercial 4.0

Recommended software licenses: the licenses to recommend when software such as a Workflow, is registered: 
  * GNU General Public License 3.0
  * GNU Lesser General Public License 2.1

Permissions Summary Settings: choose when/if to display the "Preview of your sharing settings" pop-up when creating or updating a resource 
* Always show

Authorization update batch size: the number of authorization updates to process per cycle of the job 
* 10

### Registration settings

All disabled.

## Homepage Settings

All disabled, except
* Announcement enabled
* Home page description: provide text
* Home page description position: The location of the home page description
  * Right side
* Tag cloud enabled: Display the tag cloud on the right-hand side of the home page.
* Tag threshold: Tags must have a count above or equal to this value to appear in either expanded or collapsed right-hand tag cloud
  * 1
* Maximum visible tags: The maximum number of tags that will appear in the right-hand tag cloud in its collapsed state.
  * 20

### Panels

All enabled.

## Paging/Sorting behaviour

### Index Pages

* Default items per page: The number of items shown per page on index pages by default.
  * 7
* Default items per page in condensed views: The number of items shown per page on index pages by default in condensed views.
  * 14

### Other
* Related items limit: The number of items per category displayed in the "Related items" section, before the user has to click the "View all..." link.
  * 5
* Search results limit: The number of search results per category displayed when performing a general search, before the user has to click the "View all..." link.
  * 5
