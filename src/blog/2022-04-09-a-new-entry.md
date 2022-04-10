---
title: Intro to Netlify CMS
description: Netlify CMS is an open source content management system for your
  Git workflow that enables you to provide editors with a friendly UI and
  intuitive workflows. You can use it with any static site generator to create
  faster, more flexible web projects.
author: Dismas Too
date: 2022-04-09T01:04:09.282Z
tags:
  - post
  - featured
image: /assets/blog/article-3.jpg
imageAlt: bitcoin
---
## Add to Your Site

> You can adapt Netlify CMS to a wide variety of projects. It works with any content written in markdown, JSON, YAML, or TOML files, stored in a repo on [GitHub](https://github.com/), [GitLab](https://about.gitlab.com/), or [Bitbucket](https://bitbucket.org/). You can also create your own custom backend.

This tutorial guides you through the steps for adding Netlify CMS to a site that's built with a common [static site generator](https://www.staticgen.com/), like Jekyll, Hugo, Hexo, or Gatsby. Alternatively, you can [start from a template](https://www.netlifycms.org/docs/start-with-a-template) or dive right into [configuration options](https://www.netlifycms.org/docs/configuration-options).

```
table,
td,
th {
    border: 1px solid var(--clr-neutral-300);
    text-align: left;
}

table {
    border-collapse: collapse;
    width: 100%;
}

th {
    padding-top: 12px;
    padding-bottom: 12px;
    text-align: left;
    background-color: var(--clr-primary-400);
    color: var(--clr-neutral-100);
}

th,
td {
    padding: 15px;
}

tr:nth-child(even) {
    background-color: var(--clr-primary-200);
}
```

## [](https://www.netlifycms.org/docs/add-to-your-site/#app-file-structure)App File Structure

A static `admin` folder contains all Netlify CMS files, stored at the root of your published site. Where you store this folder in the source files depends on your static site generator. Here's the static file location for a few of the most popular static site generators:

| These generators                             | store static files in |
| -------------------------------------------- | --------------------- |
| Jekyll, GitBook                              | `/` (project root)    |
| Hugo, Gatsby, Nuxt 2, Gridsome, Zola, Sapper | `/static`             |
| Next, Nuxt 3                                 | `/public`             |
| Hexo, Middleman, Jigsaw                      | `/source`             |
| Spike                                        | `/views`              |
| Wyam                                         | `/input`              |
| Pelican                                      | `/content`            |
| VuePress                                     | `/public`             |
| Elmstatic                                    | `/_site`              |
| 11ty                                         | `/_site`              |
| preact-cli                                   | `/src/static`         |
| Docusaurus                                   | `/static`             |

<!--EndFragment-->