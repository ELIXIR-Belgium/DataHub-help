---
sidebar: false
title: DataHub Documentation # Replace with instance name
---
{% assign seek_instance_name = site.seek_instance.name | default: "FAIRDOM-SEEK" %}

<!--Complete the description of your own instance here or delete it.-->
<div>
{% unless seek_instance_name == "FAIRDOM-SEEK" %}
    ## About {{ seek_instance_name }}
    The {{ seek_instance_name }} platform is based on the [FAIRDOM-SEEK](https://seek4science.org/) software.
{% endunless %}
</div>

## About FAIRDOM-SEEK

The FAIRDOM-SEEK platform is a web-based resource for sharing heterogeneous scientific research datasets,
models or simulations, processes and research outcomes. More details about FAIRDOM-SEEK can be found on the [FAIRDOM-SEEK Website](https://seek4science.org).

To see examples of FAIRDOM-SEEK being configured in hubs and projects, please visit the [FAIRDOM-SEEK In Use page](https://fair-dom.org/fairdom-in-use/) on the FAIRDOM website.
If you wish to practice using FARIDOM-SEEK without disturbing any real hubs or projects, please visit our [Demo](https://demo.seek4science.org).

<br /><br />

## Getting started

<div class="mb-5 row row-cols-1 row-cols-md-2 row-cols-lg-3 gy-4 navigation-tiles">
    <div class="col d-grid">
        <a role="button" class="btn py-3 fs-4 section-title" href="{{ '/get-seek' | relative_url }}"><h3 class=""><i class="fa-solid fa-magnifying-glass-chart fa-1x"></i> Get FAIRDOM-SEEK</h3>
        <p>Find out how to install FAIRDOM-SEEK on your own machine, or consider our public alternatives.</p>
        </a>
    </div>
    <div class="col d-grid">
        <a role="button" class="btn py-3 fs-4 section-title" href="{{ '/help/user-guide' | relative_url }}"><h3><i class="fa-solid fa-user-group fa-1x"></i> <i class="fa-solid fa-book fa-1x"></i> User guide</h3>
        <p>General documentation on how to use, administer and troubleshoot {{ seek_instance_name }}.</p>
        </a>
    </div>
    <div class="col d-grid">
        <a role="button" class="btn py-3 fs-4 section-title" href="{{ '/help/user-guide/api' | relative_url }}"><h3><i class="fa-solid fa-cloud fa-1x"></i>   API documentation</h3>
        <p>Details on how to get started using the Application Programme Interface (API).</p>
        </a>
    </div>
    <div class="col d-grid">
        <a role="button" class="btn py-3 fs-4 section-title" href="{{ '/tech/' | relative_url }}"><h3><i class="fa-solid fa-wrench fa-1x"></i> <i class="fa-solid fa-book-atlas fa-1x"></i> Technical guide</h3>
        <p>More detailed information about installation, upgrading and extended metadata.</p>
        </a>
    </div>
    <div class="col d-grid">
        <a role="button" class="btn py-3 fs-4 section-title" href="{{ '/tech/roadmap' | relative_url }}"><h3><i class="fa-solid fa-map-location-dot fa-1x"></i>  Roadmap</h3>
        <p>An outline of plans the core FAIRDOM-SEEK development team will be working on in the near future.</p>
        </a>
    </div>
    <div class="col d-grid">
        <a role="button" class="btn py-3 fs-4 section-title" href="{{ '/tech/contributing' | relative_url }}"><h3><i class="fa-solid fa-truck-fast fa-1x"></i>  Contributing</h3>
        <p>We welcome contributions to the FAIRDOM-SEEK software and these pages.</p>
        </a>
    </div>
</div>
