* Convert HTML to clean Markdown.
* Do not use underscores in metadata keywords.
    * For example, generate `wordpressid` instead of `wordpress_id`.
* Use 'published' keyword instead of 'date'.
* Generate date in ISO8601 format.
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
