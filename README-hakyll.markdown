# exitwp-hakyll

This is exitwp version taking into account requirements specific to Hakyll.

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
