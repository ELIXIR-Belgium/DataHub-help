---
title: SEEK User Guide - Browsing
layout: page
---

# Browsing content on seek

Seek contains several types of content which you can access by clicking on "Browse" from any page.

![Browse Content type dropdown](/images/user-guide/browsing_home.png){:.screenshot}

The list of results provides filtering options, which vary depending on the type of content. For example, events can be filtered by the country where they take place.

![Facet filters](/images/user-guide/browsing_filter_facets_events.png){:.screenshot}

By default, the content is listed as cards, providing title and some basic information.

![Condensed view](/images/user-guide/browsing_default.png){:.screenshot}


Alternatively, a condensed view and a table view is available, showing more results at once.
![Condensed view](/images/user-guide/browsing_condensed.png){:.screenshot}

The columns to be shown by the table view can be customised, adding/removing columns as well as choosing their order.

![Table view configuration](/images/user-guide/browsing_table_config.png){:.screenshot}

# Browsing Samples
You can browse Samples registered in SEEK by Sample Type or by Experiment Sample Templates.
* From any page, click on Browse from the top navigation bar
* Select Samples from the dropdown menu
* To query by Experiment Sample Templates, click the button "Query by Experiment Sample Templates" on the top right of the screen
* To filter by Sample Type, use the filter "Sample type" on the left side bar

<div class="alert alert-info">
Note that the ISA-JSON compliance feature must be enabled by the platform administrator for browsing by Experiment 
Sample Template to be available. 
</div>

## Browse Samples by Sample Type
Browsing Samples by Sample Type allows you to browse the samples generated by one Sample Type. Samples can be browsed based on one Sample Type at the time.
* Select the Project(s) to which the Sample Type of interest must belong. You can select Projects among
  * Your Projects: these are the Projects you are a member of that have sample types defined
  * Other Projects: these are the Projects you are not a member of that have sample types defined
* Scroll down to see the list of all selected Sample Types. Click on the Sample Type of your interest
* Click on View samples button (visible only if at least one Sample has been created with the selected Sample Type by any user) on the top right corner of the page
* Use the search boxes in each column to browse samples
* Click on Export table to export the search result as spreadsheet

## Browse Samples by Experiment Sample Template
Browsing Samples by Experiment Sample Template allows you to query the samples of interest based on Experiment Sample Template, its attributes and the attribute’s values of the samples of interest.

Moreover, Advanced filtering allows you to further refine your query based on Experiment Sample Template, its attributes and the attribute’s values of (indirect) parents and/or children (inputs and/or outputs) samples of your samples of interest.

**Query Samples**
* Select Search by Experiment Sample Template
* Select the Project(s) to which the samples of interest must belong
* Select the Experiment Sample Template used to create the samples of interest. You can also select
  * a specific Attribute of the selected Template
    * a specific value for the selected Attribute

*Advanced filtering - Input Sample(s)*
* Select the Experiment Sample Template used to create the input(s) or parent samples of your samples of interest. You can also select
  * a specific Attribute of the selected input(s) or parent samples Template
    * a specific value for the selected Attribute

*Advanced filtering - Output Sample(s)*
* Select the Experiment Sample Template used to create the output(s) or children samples of your samples of interest. You can also select
  * a specific Attribute of the selected output(s) or children samples Template
    * a specific value for the selected Attribute

* Click on Query to view your samples of interest (query’s result)
* Click on Export table to export the result of the query as spreadsheet

![Browse sample by Experiment Sample Template](/images/user-guide/isajson-compliance/browse-samples-by-isajson-template.png){:.screenshot}