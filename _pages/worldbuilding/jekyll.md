---
layout: page
title: a personal wiki with jekyll
permalink: /worldbuilding/jekyll.html
---

This is the method I use to store and organize my worldbuilding, and how to implement it if you'd like to do the same.

[Jekyll](https://jekyllrb.com/) is a [static-site generator](https://www.cloudflare.com/learning/performance/static-site-generator/): it generates your website once, making all the files ready for retrieval ahead of time. This website was built with it, because it's what Github Pages uses, but it's also a really good tool if you just want to browse your files like a website without actually publishing them on one.

The way I structure my Jekyll projects allows me to get all the HTML and CSS out of the way in a handful of files, and then all the actual content is written in Markdown.



## getting started with jekyll

Follow the instructions for your operating system [here](https://jekyllrb.com/docs/installation/) to install Jekyll.

Once you've got it installed you can create a new site by running

```
jekyll new SITE_NAME_HERE
```

If you want to use the setup I use, you can download the template at its github repository. This way it's already configured to work well with the theme.

1. go to the wiki repo and download it. unzip it into your preferred location
2. download the rubygem
3. edit your gemfile and config
4. serve the site and navigate to the localhost



## site structure

A basic Jekyll site includes the following:
+ The `_includes` folder contains snippets of HTML that are frequently reused on pages throughout the website. This saves us from having to copy and paste the HTML on multiple pages, and we only have to edit it in one file in order to change every instance of it.
+ The `_layouts` folder contains the formatting for different types of pages, meaning that instead of formatting each page individually we can just specify which layout template to use.
+ The `_sass` folder contains all the styling for the site, written in SCSS.
+ The `_site` folder contains everything that Jekyll outputs when it builds the site. Don't edit anything in this folder, as it will be rewritten the next time you serve the site.
+ The `assets` folder contains things like fonts, images, and Javascript files. It also contains a `.css` file importing all of your SCSS so that Jekyll can convert it to regular CSS; don't edit this file.
