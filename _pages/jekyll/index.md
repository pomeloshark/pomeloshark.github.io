---
   layout: page
   title: a personal wiki with jekyll
   permalink: /jekyll.html
---

This is the method I use to store and organize my worldbuilding, and how to implement it if you'd like to do the same. It requires some basic familiarity with the command line, but hopefully will be doable even for beginners; installing Jekyll itself is the most difficult part, and even then you can pretty much just copy and paste the commands from the installation guide into your terminal.

[Jekyll](https://jekyllrb.com/) is a [static-site generator](https://www.cloudflare.com/learning/performance/static-site-generator/): it generates your website once, making all the files ready for retrieval ahead of time. This website was built with it, because it's what Github Pages uses, but it's also a really good tool if you just want to browse your files like a website without actually publishing them on one.

The way I structure my Jekyll projects allows me to get all the HTML and CSS out of the way in a handful of files, and then all the actual content is written in [Markdown](https://www.markdownguide.org/).

## A note on the command line

The main thing you'll need to do via the command line is change the directory you're in, using the command `cd` followed by the path to the new directory, relative to your root directory. [Here](https://www.wikihow.com/Find-a-File%27s-Path-on-Windows) is how to find a file's path on Windows, and [here](https://macpaw.com/how-to/get-file-path-mac) is how to find it on a Mac (you can also drag and drop the folder into your terminal and it will automatically fill in the path for you). [Here](https://linuxhandbook.com/get-file-path/) are some different methods for Linux.



## Getting started with Jekyll

Follow the instructions for your operating system [here](https://jekyllrb.com/docs/installation/) to install Jekyll.

### Starting from a template

If you want to use the setup I use, you can download the template at its [Github repository](https://github.com/pomeloshark/paperwiki-example). This way it's already configured to work well with the theme.

1. Go to the [wiki repo](https://github.com/pomeloshark/paperwiki-example) and click the green 'Code' button; download the repository as a .zip file. Unzip it into your preferred location.
2. Go to your terminal and navigate to the directory by entering `cd /path/to/directory`
3. Run `bundle install` to install any missing Ruby gems, including the PaperWiki theme.
4. Now you can run `bundle exec jekyll serve`. This will generate the site, and give you the server address where you can view it, also known as your localhost. Copy and paste this server address into your browser's address bar, and you should see the following:

![A screenshot of the PaperWiki homepage.](/assets/images/homepage.png)

Your site is now functional!

### Starting from scratch

Once you've got Jekyll installed you can create a new site by running

```
jekyll new SITE_NAME_HERE
```

This will give you a very bare bones Jekyll site, with an index page, a folder for blog posts, a config file, and a Gemfile. You'll have to do a little setup to make it usable with this theme. Here's what the directory should look like:

```
.
├── _pages/
│   ├── wiki/ # In here is where your organizational pages for your wiki will go.
├── _posts/ # If you want to write blog posts, they go in here.
├── _site/
├── collections/
│   ├── _wiki/ # In here is where all your articles will go, in markdown or html files.
├── _config.yml
├── 404.html
├── about.md
├── Gemfile
├── index.md
```

(Don't worry about the .gitignore or the Gemfile.lock.)

To use this theme, open your Jekyll site's `Gemfile`, delete the line that says `gem "minima"` and replace it with this line:

```ruby
gem "jekyll-theme-paperwiki", "~> [version]"
```

And add this line to your Jekyll site's `_config.yml`:

```yaml
theme: jekyll-theme-paperwiki
```

And then execute:

```
$ bundle
```

Or install it yourself as:

```
$ gem install jekyll-theme-paperwiki
```

To serve your site locally, navigate into the site's directory and run:

```
$ bundle exec jekyll serve
```

Navigate to your localhost and...you will see an empty page. This is because the layout in the default `index.md` is not set properly. Open this file and change the layout in the front matter like so:

```yaml
---
layout: launchpad
---
```

This will show you the default wiki homepage.



## Using the wiki

The three links - explore, contents, and random page - link to pages that are included with the theme, and consist of pregenerated content based on the wiki articles you've written. Now you can start adding articles in your `_wiki` folder.




## Site structure

A basic Jekyll site includes the following:
+ The `_includes` folder contains snippets of HTML that are frequently reused on pages throughout the website. This saves us from having to copy and paste the HTML on multiple pages, and we only have to edit it in one file in order to change every instance of it.
+ The `_layouts` folder contains the formatting for different types of pages, meaning that instead of formatting each page individually we can just specify which layout template to use.
+ The `_sass` folder contains all the styling for the site, written in SCSS.
+ The `_site` folder contains everything that Jekyll outputs when it builds the site. Don't edit anything in this folder, as it will be rewritten the next time you serve the site.
+ The `assets` folder contains things like fonts, images, and Javascript files. It also contains a `.css` file importing all of your SCSS so that Jekyll can convert it to regular CSS; don't edit this file.
