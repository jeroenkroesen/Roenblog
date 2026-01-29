---
date: 2026-01-02
tags:
    - Blog
    - Featured Blogs
---

# Tinkering with Material for MkDocs

I'm a structure nerd. So when setting up my personal publishing platform, I like to think ahead about structuring it at scale. I write extensively in my [External Mind](../../external_mind/index.md), using [Joplin](https://joplinapp.org/) as the underlying app. I've engineered my [External Mind](../../external_mind/index.md) to be really easy to dump information into and really structured so it gives back information in exactly the right contexts. Ofcourse I was tempted to setup the same experience on RoenBlog. And so before having published a single letter, I found myself boxing with [Github Pages](https://docs.github.com/en/pages), [Jekyll](https://jekyllrb.com/) and later [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) to arrive at a soothing Zen structure nerd experience.
<!-- more -->

## Simple navigation

Custom navigation in Material MkDocs is relatively simple. You can specify your own navigation structure in `mkdocs.yml`. For example, the navigation at the time of writing for RoenBlog is:

```yaml
nav:
  - Home: index.md
  - Blog: blog/index.md
  - External Mind:
    - Introduction to External Mind: external_mind/index.md
  - Digital Sovereignty:
    - Digital Sovereignty: digital_sovereignty/index.md
```

***


## Adding tags for flexibility

This feature is actually enough to structure my website at the moment. But in my External Mind I like to use a flexible structure with the use of *tags*. So I decided to give the [tags plugin](https://squidfunk.github.io/mkdocs-material/plugins/tags/#listing-configuration) a try as well. I found out it is not as versatile as the tags in Joplin, but it is useable.  
  
  
### Adding tags to a page or blog post

To add one or more tags to a page or blog post, simply use the `tags` directive in the page's frontmatter:
```yaml
tags:
    - My Tag
    - Interesting
```
  
  
### Listing tagged pages
Now in any page, you can include an automatic listing of pages and blog posts with a tag like this:
```html
<-- material/tags { 
    include: [My Tag],
    exclude: [Not For Publication]
} -->
```
  
  
### Limitations

Material MkDocs tags and listings aren't very powerful. For example: there is AND combination possible in listings (displaying only pages that have *both* tag A *and* B). However, I recon this can be added by making use of custom templates and the flexibility of the underlying Jinja syntax. For now, it will have to do. 
