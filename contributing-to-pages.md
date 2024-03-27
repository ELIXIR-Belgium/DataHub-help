---
title: contributing to pages
layout: page
---

# Contributing to these pages

If you find a mistake or wish to make an improvement to these pages, you can do so. For a small mistake, just let us know by [contacting us](contacting-us.html). For other changes you can also access and edit the pages themself.

As well as the SEEK source code, these pages are also stored in GitHub at [https://github.com/seek4science/seek](https://github.com/seek4science/seek)
and served by [GitHub pages](https://pages.github.com/).

They are under the branch [_gh-pages_](https://github.com/seek4science/seek/tree/gh-pages). Pages are in [Markdown](https://help.github.com/articles/markdown-basics/) format, with a _.md_ extension, but get converted into HTML for you.
New pages require a formatter at the top, that looks like:

    ---
    title: my lovely page
    layout: page
    ---

For example, this page can be found at [https://raw.githubusercontent.com/seek4science/seek/gh-pages/contributing-to-pages.md](https://raw.githubusercontent.com/seek4science/seek/gh-pages/contributing-to-pages.md)

If you want to view your changes as you edit them, with Ruby installed you can install and run Jekyll with:

    gem install bundler
    bundle install
    bundle exec jekyll serve

and then goto [localhost:4000/seek/](http://localhost:4000/seek/). For more information please see [Using Jekyll with Pages](https://help.github.com/articles/using-jekyll-with-pages/)

You can make a change by forking and issuing a pull request. If contributing through GitHub is unfamiliar to you, please read [Contributing to Open Source on GitHub](https://guides.github.com/activities/contributing-to-open-source/)

# Working with DataHub documentation

## FAIRDOM-SEEK documentation

FAIRDOM-SEEK documentation is in branches of the GitHub repository seek4science/seek
* gh-pages:
* gh-pages-1.13:
* gh-pages-master:
* gh-pages-sample-update: temporary branch to record features agreed upon during sample working group

## DataHub documentation

FAIRDOM-SEEK documentation (gh-pages branches) has been cloned in GitHub
* ELIXIR-Belgium/DataHub-help: to deploy documentation of the production instance (https://datahub.elixir-belgium.org)
* ELIXIR-Belgium/DataHub-help-test: to deploy documentation (https://help.datahub-test.elixir-belgium.org) of the test instance (https://datahub-test.elixir-belgium.org). Forked from ELIXIR-Belgium/DataHub-help.
* ELIXIR-Belgium/DataHub-help-usecase: to deploy documentation (https://help.datahub-usecase.elixir-belgium.org) of the usecase instance (https://datahub-usecase.elixir-belgium.org). Forked from ELIXIR-Belgium/DataHub-help.

## How to contribute to DataHub documentation

### General way of working
1. Use [ELIXIR-Belgium/DataHub-help-test](https://github.com/ELIXIR-Belgium/DataHub-help-test) to propose changes to the DataHub documentation pages.
2. DataHub team will review and approve/reject your changes.
3. DataHub team will push the changes towards ELIXIR-Belgium/DataHub-help.

### via GitHub GUI
1. Go to [ELIXIR-Belgium/DataHub-help-test](https://github.com/ELIXIR-Belgium/DataHub-help-test).
2. Make the changes you want to propose.
3. Open a pull request from your fork (that is created by GitHub by default) towards ELIXIR-Belgium/DataHub-help-test. 

   *IMPORTANT: please check that your pull request is against **DataHub-help-test main**  and not DataHub-help.*

4. Follow up via GitHub for comments from the DataHub team.

### via code editor of your choice (e.g. VSCode)

This is a general workflow in how to work on your own fork (copy) of the repository and request changes through a pull request.
1. In GitHub, make a fork of [ELIXIR-Belgium/DataHub-help-test](https://github.com/ELIXIR-Belgium/DataHub-help-test) using the fork button. Then go to `Code --> SSH --> copy`
2. Open a terminal and choose a directory. Then clone your fork there using:
    ```
    git clone git@github.com:USERNAME/DataHub-help-test.git
    cd DataHub-help-test
    ```
    NOTE: Make sure you clone the fork and not the original ELIXIR-Belgium/DataHub-help-test one.
3. Set your fork of DataHub-Help (e.g. username/DataHub-help) as your **remote**
4. Set ELIXIR-Belgium/DataHub-help-test as your **origin**
5. When making changes
* Keep your fork up to date by pulling from **origin** (ELIXIR-Belgium/DataHub-help-test).
* Create a new branch named after your feature/edit and make the changes you want to make.
* Commit and push to **remote** (e.g. username/DataHub-help).
6. In GitHub, open a pull request and make sure to set ELIXIR-Belgium/DataHub-help-test main as base repository.

   *IMPORTANT: please check that your pull request is against **DataHub-help-test main**  and not DataHub-help.*
