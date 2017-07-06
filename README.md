# Project Docs

A software project theme for [Hugo](https://gohugo.io).

## Quick start

Inside your website's theme directory, install the theme with `git`:


  git clone https://github.com/lrntct/hugo-project-doc.git


Next, take a look in the `exampleSite` folder.
This directory contains an example configuration file and the content for the demo.
It serves as an example setup for your documentation.

Copy its content in the root directory of your website.
Overwrite the existing config file if necessary. 

The style sheets are written in [scss](http://sass-lang.com/) and therefore need to be compiled into CSS before the site could be used.
You can do it like so:

  sass -t compressed _sass/main.scss:static/css/main.css

Hugo includes a development server, so you can view your changes as you go.
Start it up with the following command:

  hugo server

Now you can go to [localhost:1313](http://localhost:1313) and the Material theme should be visible.

To compile your site to the disk, just type `hugo` in the main directory.


## Acknowledgements

This theme is a partial port of the [jekyll-doc-theme](https://github.com/aksakalli/jekyll-doc-theme) from Can Güney Aksakalli.
It takes some snippets from the [DocDock](https://github.com/vjeantet/hugo-theme-docdock)
and [hugo-academic](https://github.com/gcushen/hugo-academic) themes, written by Valere Jeantet and George Cushen, respectively.
This README  is inspired by [hugo-material-docs](https://github.com/digitalcraftsman/hugo-material-docs) from Digitalcraftsman.


## License

The theme is released under the MIT license. Read the [license](https://github.com/lrntct/hugo-project-doc/blob/master/LICENSE.md) for more information.

