# exitwp-hakyll

Port of Thomas Frössman's [exitwp](https://github.com/thomasf/exitwp) tool.

exitwp-hakyll is tool for making migration from one or more wordpress blogs to the [Hakyll](https://jaspervdj.be/hakyll/) static sites generator as easy as possible.

The latest version at https://github.com/mloskot/exitwp-hakyll

## Requirements

* Python 2.x
* BeautifulSoup
* See import statements at the top of exitwp-hakyll.py 

## Features

* Convert HTML to clean Markdown.
* Do not use underscores in metadata keywords.
    * For example, generate `wordpressid` instead of `wordpress_id`.
* <strike>Use 'published' keyword instead of 'date'.</strike> - Hakyll's got 'date' field support.
* <strike>Generate date in ISO8601 format.</strike> - Hakyll's got relaxed ISO8601 ('T' replaced wth space, no 'Z') format support.
* Flat format of taxonomy tags output:
```
categories: open source, programming
tags: python, web
```
instead of Jekyll variant:
```
categories:
- open source
- programming
tags:
- python
- web
```
* Support two mode output build:
    * Flat with dates encoded in filenames: YYYY-MM-DD-my-post.markdown
    * Tree of folders based on dates: YYY -> MM -> DD -> my-post.markdown
* Minor formatting improvements.
