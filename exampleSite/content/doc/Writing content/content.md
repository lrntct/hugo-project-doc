+++
title = "Writing content"
weight = 10
+++

In Hugo, all the site content is located within the `content` directory.
Please have a look in the `exampleSite` folder and see how content is organised.

## Sections

The main sections appears on the top navigation bar.
Every section is a folder in the `content` directory.
Additionally to the home page, there is two special types of sections: `doc` and `blog`.
Those two use a specific layout for documentation and blog posts.
To use those layouts, the folder where they are should be named this way.
Other sections will use the default layout.

In each section, put a `_index.md` file with the following [front matter](https://gohugo.io/content/front-matter/):

```
+++
title = "The section title"
weight = 10
+++
```

The weight value decides the relative order in which the sections are displayed in the menu.
The higher the value, the later the section will appear in the navigation bar.

## Home page

The home page comprised three types of content:

1. A *jumbotron* or *hero*, with text above a background image,
2. a two columns container with text on the left and an image on the right,
3. a three cards container, each with a title, an icon and a text body.

The content files for the home page should be placed inside the `home` directory.

### Jumbotron

To use the jumbotron, the content file must contain the following elements in the front matter:
```
title = "Your big message"
type = "jumbotron"
bgImage = "/img/your-background-image.jpg"
```
The content of the file will appear inside the hero.

### Two-columns container

To create a two-columns container, the content file must contain the following information:
```
image = "img/hugo-logo.png"
type = "text_img"
```

With image being the image drawn on the right column.

### Three cards container

Each card must have the `type = "card"` in the front matter.
The front matter should looks like that:
```
+++
icon = "a font awesome code"
title = "Publish with git"
type = "card"
+++
```
*icon* is a [Font Awesome](http://fontawesome.io) icon without the leading *fa-*.
For example, if you want to use "fa-snowflake-o", just write "snowflake-o".
The content body will be used for the text field of each card.

## Documentation

To use the specific documentation layout, the documentation should be placed in the `doc` directory of the main `content` folder.
A file named `_index.md` should be created inside to set the name and place in the main navigation bar (see above).
The documentation should be organized in subsections.
Create one directory under the `doc` folder for each subsection.
In each one, create a file named `_index.md` with the name in the front matter.
To create a new documentation page, type the following in the terminal:

```sh
hugo new doc/my-subsection/my-page.md
```

This will automatically create a new content page, with default setting in the front matter.
Each content file could be given a weight that influence its relative place within the section.

## Blog posts

Blog post should be placed inside the `blog` directory.
A file named `_index.md` should be created inside to set the name and place in the main navigation bar (see above).
The blog is not divided in subsections.
Blog posts are classified by the date given in the front matter.
The following command will create a new blog post filled with the front matter:

```sh
hugo new blog/my-blog-post.md
```
