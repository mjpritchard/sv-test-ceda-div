---
author: Matt Pritchard
title: Editing guide
description: Editing guide for the CEDA website
layout: docs
---

## Introduction

This site is built with a the {{<link "hugo">}}Hugo{{</link>}} static site builder using the {{<link "hinode_docs">}}Hinode theme{{</link>}},
with styling customised for CEDA. This guide covers how to edit and update the various sections of the site.

## Site layout

Content is organised into the following main sections:

- News
- Events
- Projects
- About

and is written in Markdown format, but with a few extra features provided by both {{<link "hugo">}}Hugo{{</link>}} and the {{<link "hinode_docs">}}Hinode theme{{</link>}} template. It is worth reading the documentation for both of these to understand the syntax fully.

Two further links in the site's navbar point to components whose content is managed elsewhere:

- **Status**
  - CEDA/JASMIN service status: this page is a single-page section of this site that renders a JSON feed of events, content for which is stored in the {{<link href="https://github.com/cedadev/ceda-status">}}ceda-status{{</link>}} repository.
- **Techblog**
  - an external link to the separately-hosted CEDA TechBlog, maintained {{<link href="https://github.com/cedadev/tech-blog">}}here{{</link>}}

The site uses a system of templates to transform content in markdown format, into a set of static web pages. So all the different views
of the site are pre-generated. So instead of there being an "admin" interface to edit the website as with previous platforms,
editing is done by changing/adding to the source content, or modifying templates or configuration, then re-building the site.

## Overview of publishing process

New content gets published when the site is rebuilt. The site gets rebuilt when:

- changes are pushed or merged to the `main` branch of the repository
- on a schedule, once every weekday night.

After [initial setup](#initial-setup-and-using-vscode-to-help-with-the-edit-process), the edit/update process involves:

1. pulling the latest changes to the site repo into your local copy (VSCode can do this for you)
1. making a branch for your edits
1. making some changes (e.g. adding a new news item)
1. checking that a LOCAL preview of the site looks OK with your changes
1. committing your changes to your branch (in the version of your repo)
1. pushing that branch to the remote repository (Github)
1. checking that a REMOTE preview of the site looks OK with your changes (a remote preview is generated for each branch automatically)
1. creating a pull request to merge that branch into `main`
1. reviewing the pull request, see {{<link "#roles"/>}}
1. merging the pull request, see {{<link "#roles"/>}}
1. waiting for the site to be rebuilt
1. checking that all is OK with the rebuilt live site

## Roles

The following roles are in use for this site (corresponding to groups in our GitHub org). Your GitHub ID needs to be a member of the relevant group(s).

- **ceda-div-site-authors**
  - can create content for review & publication by an editor
- **ceda-div-site-editors**
  - can merge changes for publication to the live site

## Editing a news item

Your route to editing a news item will depend on your role:

- Authors might prefer to create/edit new news items in the GitHub site itself, submitting them for review and publication by an Editor
  - {{<link "editing-a-news-item#authors">}}see this process in detail{{</link>}}
- Editors would do the whole process themselves, using a local install of Hugo and Hinode to work on changes to the site, or
reviewing and merging changes proposed by an editor. They might ask another Editor to review their own changes.
  - {{<link "editing-a-news-item#editors">}}see this process in detail{{</link>}}

News items are stored in the directory `content/news/updates/YYYY` where `YYYY` is the current year.

There is a template news item here, which can be copied as an example:

`content/news/updates/2024/2024-03-06-an-example-news-item.md`

But to do this, note the following:

- the filename should be of the form `YYYY-MM-DD-slug.md`, where
  - `YYYY-MM-DD` is the publication date. If the year is 2024, this file should go in the `2024` directory.
  - `slug` is a CONCISE string **representing** the title (doesn't have to be identical)
  - `.md` format extension needs to be present, but is not used in the eventual URL of the article

Inside the markdown file we have:

```markdown
---
title: An example news item
date: 2024-03-06 10:30:00
tags: ['news', 'ceda']
thumbnail: 
icon: fas circle-info text-info
draft: true # remove this line in your copy
---

No need to repeat the title as a heading here.
This is an example news item which can be copied to create a new one.

### Here's a heading

Here's some text (after a spacer line)

#### A subheading

And some more text, just before the blank line at the end.

```

Looking at the top section first:

- The "Frontmatter" or metadata section is at the top of the file, between the separators `---` and `---`.
[Hugo allows frontmatter](https://gohugo.io/content-management/front-matter/#overview) in YAML, TOML or JSON syntax: the separator symbol denotes which:  `---` is for YAML. For this site, to keep things simple, we'll stick to YAML as used above.
- There should be a blank line after the separator and before the markdown content, and also at the end of the file (see {{<link "#markdown-source-files"/>}}).

For a full explanation see the {{<link "https://gethinode.com/docs/content/content-management/#front-matter">}}documentation on Hinode Frontmatter{{</link>}},
but the Frontmatter fields used above (and sufficient for a simple news item) are:

field | content | comment
--- | --- | ---
**title** | Title of the post | Avoid quotes, ampersands or other symbols, be consistent with capitalisation. Don't repeat the title in the markdown: the template does this for you in list & single views. Add other headings starting with `### Heading3` (because `title` gets rendered as `## Heading2`).
**date** | Publication date/time of the post | Must be in the format `YYYY-MM-DD hh:mm:ss` including the time with seconds. The date part should correspond with the filename. Articles with a date in the future are NOT built, so you can use this to schedule future publication, but only if the site is rebuilt at some point before that date.
**tags** | Tags relevant to this post | Check first to choose from {{<link "/tags">}}existing tags{{</link>}} or add your own. Take care with typos not to create new ones unnecessarily.
**thumbnail** | Optional image for the post | An image specified here will be used as the thumbnail for the post in list view, and as a banner across the top of the post in single view. It should exist in a corresponding directory `assets/img/YYYY/YYYY-slug/`, so you need to create that directory and add that image file in your changes, in order to refer to it. <br>**A post should have either an image OR an icon, with the other field left blank**
**icon** | Optional icon for the post | Should be in format `<icon-library> <icon-name> text-<colour>` using the name of an icon from {{<link "https://fontawesome.com/search?o=r&m=free">}}FontAwesome icons{{</link>}} (filtered for "free" ones).<br>`<icon-library>` can be either `fa`, `fab` or `fas`, shorthand for `fa-regular`, `fa-brands` or `fa-solid`.<br>`<icon-name>` should be the name of the icon but witout the `fa-` prefix.<br>`text-<colour>` is optional but the `<colour>` choice is from this site's predefined theme colours, i.e.<br>{{< badge title="primary" color="primary" >}}(default) {{< badge title="secondary" color="secondary" >}}{{< badge title="success" color="success" >}}{{< badge title="danger" color="danger" >}}{{< badge title="warning" color="warning" >}}{{< badge title="info" color="info" >}}{{< badge title="light" color="light" >}}{{< badge title="dark" color="dark" >}}.  <br>**A post should have either an image OR an icon, with the other field left blank**
{.table .table-striped}

Once the rest of the content of the news item has been written, you're at {{<link "#overview-of-publishing-process">}}step 3 of the publishing process{{</link>}}, so follow the remainder of the process to get the item published.

## What is markdown?

{{<link "https://en.wikipedia.org/wiki/Markdown">}}Markdown{{</link>}} is very lightweight markup language for creating formatted text. It's intended to be easy to read in its basic form, but the Hugo and Hinode systems used here add some additional functionality by using shortcodes and other features, which help specifically in the creation of richly-formatted static websites.

## Style guidelines

We want to keep the site looking smart, engaging and easy to read.

By using a well-maintained set of tools and taking care with authoring, reviewing and publishing content on the site, this is now more achievable than with previous platforms, using the tips and guidelines below.

### Markdown source files

- VSCode supports editing and preview of markdown files without installing anything new
  - good for a basic, quick view and for proofreading
- Install and use the David Anson / `markdownlint` {{<link "https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint">}}markdown linter for VScode{{</link>}}
  - this helps keep markdown content tidy and functional
  - for example: preferred syntax for lists, whitespace, headings, etc.
  - (rather than list all the rules here, use the linter and discover better markdown syntax!)
  - it doesn't support ALL the formatting we might want to use, but we could extend the rule set. Exemptions can be declared (see source for this article, around the `example` shortcode)
- Managing the source content using `git` we have better control of the process
  - Use VSCode's `git` integrations to help with managing your changes to the site

### Content

#### General

- Be concise :wink:

#### Links

- Use labelled links instead of describing what to do: avoid "please follow the link below"
- Use a {{< button color="primary" href="#!" button-size="md" >}}button{{< /button >}} to make important links or actions visually distinct
- In-page links are automatically generated from subheadings (hover to see them), so don't make your own.
- Use the {{<link "https://gethinode.com/docs/components/link/">}}link{{</link>}} shortcode where possible, as this makes it easier to control their appearance throughout the site. But if you can't bothered, the `[markdown](#url)` format works too.
- You can link to things by name, slug, url or (if needed) path to the markdown file. See the `link` documentation for examples.
- Use a relative link if at all possible, this makes changes to the site easier
- There's a curated set of frequently-used links (e.g. `"ceda_archive"`) in `config/_default/params.toml`: consider adding to this list for frequently-used links: this means they can be used throughout the site but updated in one place if things change.
- We can create a curated set of abbreviations, stored in `data/abbr.yml`, for use with the {{<link "https://gethinode.com/docs/components/abbr/">}}abbr{{</link>}} shortcode, for example {{<abbr ceda >}} (hover for details).

### Images

(see {{<link "https://gethinode.com/docs/components/image/">}}Hinode docs{{</link>}})

Hinode has some clever image-formatting features, see {{<link "https://gethinode.com/docs/components/image/">}}Hinode docs{{</link>}} for details.

Store images for a news item post in `assets/img/YYYY/YYYY-slug/` and choose one of them as the thumbnail. Others can be referred to in the text 
using the `image` shortcode, e.g.

{{< example lang="hugo" show-preview="false" >}}
{{</* image src="img/flowers.jpg" ratio="3x2" caption="image caption" */>}}
{{< /example >}}

Note that although the image is stored below `assets/img`, the path starts with `img/` for the shortode. Add captions. Read the docs for why.
Use `wrapper` classes to control the size & how the image is displayed.

### Code and commands

Hugo supports {{<link "https://gohugo.io/content-management/syntax-highlighting/#list-of-chroma-highlighting-languages">}}Chroma syntax-highlighting of a huge list of languages{{</link>}}, and Hinode provides shortcodes for some of these.
Use the {{<link "https://gethinode.com/docs/components/command-prompt/">}}command-prompt{{</link>}}
or {{<link "https://gethinode.com/docs/components/example/">}}example{{</link>}}
shortcodes to render examples smartly,

<!-- markdownlint-disable MD037 -->
{{< example lang="hugo" >}}
{{</* command user="user" host="sci1" */>}}
export MY_VAR=123 ## comment
(out)command output
{{</* /command */>}}
{{< /example >}}
<!-- markdownlint-enable MD037 -->

 or use {{<link "https://gohugo.io/render-hooks/code-blocks/">}}code blocks
{{</link>}} to apply syntax highlighting.

```python
import something

print("hello world")
```

Use `inline code`highlighting to show paths or filenames like `/home/users/<username>`.

Some of these features are more suited to documentation (hence also using Hinode for the JASMIN Help Docs site),
but if we're including this sort of information in news items then these features help make it easier to
read and more engaging as content.

#### Other formatting components

- Use **alerts** to really grab attention

{{<alert alert-type="info">}}
This is an alert of type `"info"`
{{</alert>}}

{{<alert alert-type="danger">}}
This is an alert of type `"danger"`
{{</alert>}}

See the full set of {{<link "https://gethinode.com/docs/components/">}}Hinode formatting components{{</link>}} for further ideas to brighten up content.

The table of contents shown in the right sidebar of this page is generated automatically from the headings in the markdown, but only for documents in the `docs` section of the site (not currently linked in the navbar), as these section has a particular layout applied to it, see Hinode documentation on {{<link "https://gethinode.com/docs/content/content-management/">}}Content Management{{</link>}}.
Similarly, the left sidebar navigation menu only appeats for the `docs` section of the site. Its contents is controlled by the file `data/docs.yml`, see 

## Editing an event

## Editing a Project

## Editing the About pages

## Making other changes to the site

### Configuration

Cofiguration files are stored in...

### Layouts

The `layouts` directory contains...

## Initial setup and using VSCode to help with the edit process
