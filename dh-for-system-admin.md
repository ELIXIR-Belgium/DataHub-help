---
title: Deploy FAIRDOM-SEEK as DataHub
permalink: /deploy-datahub
custom_repo_url: https://github.com/ELIXIR-Belgium/datahub-test-documentation
custom_repo_branch: datahub-latest-documentation
---

Should you want to deploy your own DataHub-like instance of FAIRDOM-SEEK, you can follow this guide.
As system administrator, you have access to the Server admin panel. You can go to the Server admin panel by selecting your Name/account at the top right corner and selecting "Server admin" from the dropdown menu.

## The admin panel in the web UI
Configuring the following settings in the admin panel, will give you the same functionalities in DataHub:

### SEEK services
- Solr search engine: enabled
- Filtering: enabled

### SEEK features
- Single page: enabled
- compliance with ISA-JSON schemas: enabled

### Resource types
- Programmes: enabled
  - User creation of Programmes: enabled
- File templates (optional): disabled
- Organisms (optional): disabled
- JWS Online (optional): disabled

## Initializer file

Alternatively, you can include an initializer file in `config/initializers` with your configurations. An example file:

```ruby
SEEK::Application.configure do
# Required for DataHub
  Seek::Config.solr_enabled = true
  Seek::Config.filtering_enabled = true
  Seek::Config.programmes_enabled = true
  Seek::Config.programme_user_creation_enabled = true
  Seek::Config.project_single_page_enabled = true
  Seek::Config.isa_json_compliance_enabled = true

# Optional configurations
  Seek::Config.jws_enabled = false
  Seek::Config.organisms_enabled = false
  Seek::Config.file_templates_enabled = false
end
```

**Important:** When using the initializer file, you statically lock the settings to the provided value, meaning they cannot be changed through the web UI anymore.
