---
title: Easy to get going
weight: 10
---

Super easy, I was able to set up everything (including creating a github repo etc.) in just 2 hours. With a lot of [great documentation for beginners](https://gohugo.io/overview/quickstart/).
Basic steps are:

## Create the website

```
hugo new site <new_project>
```

## Install the theme

Install a theme by following [this documentation](https://gohugo.io/themes/installing/) for getting a theme from a Git repo.

Alternatively, you can download the theme as .zip file and extract it in the `themes` directory

## Basic configuration

Hugo generates a file (`config.toml`) to configure your site. This file could also be a .yaml or .json file.

```toml
baseURL = "/"
languageCode = "en-US"

title = "Blueriq Documentation Demo"
metaDataFormat = "yaml"
contentDir = "D:/Users/j.van.de.sant/Documents/devenv/poc-md/"
theme = "hugo-theme-learn"

[params]
  editURL = "https://github.com/jaapsant/poc-md/tree/master/"
```

## Create a page

With a theme you get some archetypes to create skeletons for your website. Creating pages based on these archetypes is very easy. 
In the example below, the archetype is chapter.

```
hugo new --kind chapter basics/_index.md
```

The theme used has 2 archetypes: _chapter_ or _content_ where _content_ is set as default. So generating a content page is as easy as one of these:

```
hugo new basics/first-content.md
hugo new basics/second-content/_index.md
```

## Launching the website locally

Launch by using the following command:

```
hugo serve
```

Go to `http://localhost:1313`


## Build the website

When your site is ready to deploy, run the following command:

```
hugo
```

A `public` folder will be generated, containing all static content and assets for your website. It can now be deployed on any web server.