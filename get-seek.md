---
title: Get FAIRDOM-SEEK
description: Installation guide, where to start, and alternative public instances available for use. 
sidebar: get_fairdom-seek
redirect_from: "/get_seek.html"
---

FAIRDOM-SEEK is open source software, and is distributed under a [BSD License](https://github.com/seek4science/seek/blob/main/BSD-LICENSE). The source code is all available on [GitHub](https://github.com/seek4science/seek).




## I want to install FAIRDOM-SEEK, where do I start?

<div class="row row-cols-1 row-cols-md-2 row-cols-lg-3 gy-4 where-start">
    <div class="col d-grid ">
        <div class="where-start-tile  bg-light">
            <h3>Installation and upgrade</h3>
            <p>For details on how to install FAIRDOM-SEEK please refer to our <a href="{{ "/tech/install" | relative_url }}">Installation Guide</a>.</p>
            <p>For details on how to upgrade an existing FAIRDOM-SEEK installation please refer to our <a href="{{ "/tech/upgrading" | relative_url }}">Upgrade Guide</a>.</p>
        </div>
    </div>
    <div class="col d-grid">
        <div class="where-start-tile bg-light">
           <h3>Docker</h3>
            <p>FAIRDOM-SEEK can also be deployed using <a href="https://docker.com">Docker</a>, for which we provide Docker images. Please read our <a href="{{ "/tech/docker" | relative_url }}">Docker guide</a>.</p>
        </div>
    </div>
    <div class="col d-grid">
        <div class="where-start-tile bg-light">
            <h3>New features and changes</h3>
            <p>To review changes and new features introduced between FAIRDOM-SEEK versions please visit our <a href="{{ "/tech/releases/" | relative_url }}">Change Log</a>.</p>
        </div>
    </div>
</div>



## Alternative: use one of the public instances of FAIRDOM-SEEK
{% include callout.html type="tip" content="
If you do not want to install your own version of FAIRDOM-SEEK, you can register to use one of the [public instances](https://fair-dom.org/fairdom-in-use/). For example, see [DataHub](https://datahub.elixir-belgium.org), a version of FAIRDOM-SEEK which is hosted by [Elixir Belgium](https://www.elixir-belgium.org/) for general community use.
" %}

### What are the differences?

| ![DataHub logo][hub]{:height="64px"} <br />DataHub public hub | ![SEEK logo][seek] <br /> Your own FAIRDOM-SEEK installation |
| ------------------------------------------------------------- | ------------------------------------------------------------ |
| Requires registration                                         | Requires installation\* and hosting                          |
| Managed by Elixir Belgium                                     | Managed by your technical team                               |
| Registry for data, operating procedures and models            | Registry for your choice of content                          |
| Open and public                                               | Can be open, public or private                               |

[hub]: {{"/images/datahub_logo2.svg" | relative_url }}
[seek]: {{ "/images/fairdom_seek_logo.png" | relative_url }}

**\*Note:** Please have a look at our ['Deploy FAIRDOM-SEEK as DataHub']({{ "/deploy-datahub" | relative_url }}) guide for applying the right configurations.
