[![Build Status](https://travis-ci.org/ClimateFAST/website.svg?branch=master)](https://travis-ci.org/ClimateFAST/website)

# FAST Climate Website

Live version (corresponds to gh-pages branch) can be found here: [fastclimate.info](http://fastclimate.info)

## Quickstart

For simple content additions you can use [prose](http://prose.io/) and proceed as described in posting guide below.

#### Local Preview

You need a version of [ruby](https://www.ruby-lang.org/en/downloads/) (at least v2) installed.
The recommended way is via [rvm](https://rvm.io/).

Check out this repository somewhere, for example `git clone git@github.com:ClimateFAST/website.git`

In the `website` folder run `bundle exec jekyll serve`.
It should pull dependencies and then build the website and run a local server on [localhost:4000](http://localhost:4000).

### Posting Guide
To create an event post, create a file in the `_posts` folder in the following format: `YYYY-MM-DD-title.md`, for example `2016-10-18-testpost.md`.
Begin that file the following lines:

```Markdown
---
type: post
categories: <comma separated list of categories>
author: <your author id>
---
```

Author ids are defined in `_data/authors.yml`. Add one for yourself if none exists.
More options for the front matter block can be found in the [jekyll-docs](https://jekyllrb.com/docs/frontmatter/).
After the front matter you can write your content using [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) formatting.

#### Pages
In order to add a new page instead of a post, add a file to the `_pages` folder with just `title.md` format.
Add the following frontmatter:

```Markdown
---
permalink: </title>
title: <Title>
layout: splash
author_profile: false
header:
 overlay_image: mountains.jpg
 caption: "Photo credit: [*8moments*](http://8moments.deviantart.com/art/Background-mountains-brunnkogel-blue-639658674)"
---

{% include references.html %}
```

Change the `permalink` and `title` fields to the desired values and write your content afterwards.

You can include references by adding an entry of the form `linkid: link-address` into `_data/references.yml` and inserting the markdown `[linktext][linkid]` into the text where the reference is supposed to appear.


## Publishing
Pushing to the `master` branch on Github automatically publishes the website if the [travis](https://travis-ci.org/ClimateFAST/website) build succeeds.
The same happens when saving in [prose](http://prose.io/).