---
   layout: index
---

## Page structure

### Table of contents

The layout of the wiki pages (and other types of entry pages, if you're using them) support up to three levels of heading: `h1` is reserved for the page title, and beyond that styling has been applied only to `h2` and `h3`, just to avoid things getting overly complicated. These two headings will be automatically retrieved and formatted into a table of contents, listed to the left of the main article.

### Sidebar

The sidebar to the right is controlled by your front matter. Notice that this page's front matter contains an array `other_projects`, under which is listed any other projects that contain an entry with the same name. This may be useful if, say, you want to write a wiki article on a piece of literature, and then link to the text of that piece of literature in another collection; or maybe write a wiki article on the history and usage of a language, and then link to a grammar or dictionary of that language. Obviously if you don't have any other collections to link to, just omit this bit of front matter.

You can include as many images as you want in a page, but if you want the page to have a header image, you can specify that using the `image` key in your front matter. The value can be a URL, or a relative link such as `/assets/images/image.png`. The image and any associated caption (optional, but recommended) will be wrapped in `figure` and `figcaption` tags.

The last two sidebar components are `quickstats` and `quicknotes`. Any key-value pairs under `quickstats` will be iterated through in table form, while `quicknotes` contains any other data that doesn't fit in a table --- this might be where you put, say, the signature of a famous person, or the motto of a university.

Any of these elements can be omitted.



## Linking

Markdown links are written like so:

```
[Text to be linked](/wiki/sample-page)
```

However, it's also possible to link to pages in your site using Liquid's `link` tag. This way, you can link to the relative path of the page, instead of the page's permalink, and it will automatically retrieve the permalink for you:

```
{%- raw -%}
[Text to be linked]({% link _wiki/Sample page.md %})
{% endraw %}
```

The output is the same as the pure Markdown link, but with one key difference: if the page you link to does not exist, Jekyll will alert you and will fail to build, so that your site cannot be built with broken links. This is a very useful feature if you are dealing with a large number of pages.

Remember that this method is case sensitive. More on linking in the [Jekyll docs](https://jekyllrb.com/docs/liquid/tags/).



## Blockquotes

A paragraph (from the Greek paragraphos, “to write beside” or “written beside”) is a self-contained unit of a discourse in writing dealing with a particular point or idea. A paragraph consists of one or more sentences. Though not required by the syntax of any language, paragraphs are usually an expected part of formal writing, used to organize longer prose. This is just a paragraph to show what a blockquote looks like when surrounded by normal text.

   <figure>
      <blockquote cite="http://">
         <p>A block quotation (also known as a long quotation or extract) is a quotation in a written document, that is set off from the main text as a paragraph, or block of text.</p>

         <p>It is typically distinguished visually using indentation and a different typeface or smaller size quotation. It may or may not include a citation, usually placed at the bottom.</p>

         <figcaption>
            &mdash; Firstname Lastname, <cite>Title of Work</cite>
         </figcaption>
      </blockquote>
   </figure>

A paragraph (from the Greek paragraphos, “to write beside” or “written beside”) is a self-contained unit of a discourse in writing dealing with a particular point or idea. A paragraph consists of one or more sentences. Though not required by the syntax of any language, paragraphs are usually an expected part of formal writing, used to organize longer prose. This is just a paragraph to show what a blockquote looks like when surrounded by normal text.



## Lists

A paragraph (from the Greek paragraphos, “to write beside” or “written beside”) is a self-contained unit of a discourse in writing dealing with a particular point or idea. A paragraph consists of one or more sentences. Though not required by the syntax of any language, paragraphs are usually an expected part of formal writing, used to organize longer prose. This is just a paragraph to show what a definition list looks like when surrounded by normal text.

First Term
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.

A paragraph (from the Greek paragraphos, “to write beside” or “written beside”) is a self-contained unit of a discourse in writing dealing with a particular point or idea. A paragraph consists of one or more sentences. Though not required by the syntax of any language, paragraphs are usually an expected part of formal writing, used to organize longer prose. This is just a paragraph to show what a definition list looks like when surrounded by normal text.

1. First item
2. Second item
3. Third item

A paragraph (from the Greek paragraphos, “to write beside” or “written beside”) is a self-contained unit of a discourse in writing dealing with a particular point or idea. A paragraph consists of one or more sentences. Though not required by the syntax of any language, paragraphs are usually an expected part of formal writing, used to organize longer prose. This is just a paragraph to show what a definition list looks like when surrounded by normal text.

- First item
- Second item
  - Sub item
- Third item

A paragraph (from the Greek paragraphos, “to write beside” or “written beside”) is a self-contained unit of a discourse in writing dealing with a particular point or idea. A paragraph consists of one or more sentences. Though not required by the syntax of any language, paragraphs are usually an expected part of formal writing, used to organize longer prose.



## Sidenotes

A paragraph<sup>1</sup> <span class="aside"><sup>1</sup> (from the Greek paragraphos, “to write beside” or “written beside”)</span> is a self-contained unit of a discourse in writing dealing with a particular point or idea. A paragraph consists of one or more sentences. Though not required by the syntax of any language, paragraphs are usually an expected part of formal writing, used to organize longer prose.

---

A paragraph (from the Greek paragraphos, “to write beside” or “written beside”) is a self-contained unit of a discourse in writing dealing with a particular point or idea. A paragraph consists of one or more sentences. Though not required by the syntax of any language, paragraphs are usually an expected part of formal writing, used to organize longer prose.



## Tabular data

A paragraph (from the Greek paragraphos, “to write beside” or “written beside”) is a self-contained unit of a discourse in writing dealing with a particular point or idea. A paragraph consists of one or more sentences. Though not required by the syntax of any language, paragraphs are usually an expected part of formal writing, used to organize longer prose.

   <table>
      <caption>table caption</caption>
      <thead>
         <tr>
            <th>table heading</th>
            <th>table heading</th>
            <th>table heading</th>
            <th>table heading</th>
            <th>table heading</th>
         </tr>
      </thead>
      <tbody>
         <tr>
            <td>table data</td>
            <td>table data</td>
            <td>table data</td>
            <td>table data</td>
            <td>table data</td>
         </tr>
         <tr>
            <td>table data</td>
            <td>table data</td>
            <td>table data</td>
            <td>table data</td>
            <td>table data</td>
         </tr>
         <tr>
            <td>table data</td>
            <td>table data</td>
            <td>table data</td>
            <td>table data</td>
            <td>table data</td>
         </tr>
         <tr>
            <td>table data</td>
            <td>table data</td>
            <td>table data</td>
            <td>table data</td>
            <td>table data</td>
         </tr>
      </tbody>
   </table>



## Miscellaneous

   <p>Keyboard input: <kbd>Cmd</kbd></p>
   <p>Inline code: <code>&lt;div&gt;code&lt;/div&gt;</code></p>

### Pre-formatted text

```
$ gem bundle install
```
