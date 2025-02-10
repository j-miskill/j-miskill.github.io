# What this repo is

Repository for my personal website. Hosted using GitHub pages, built using Jekyll. 

## Notes

Objects, tags, and filters in Liquid. Objects are `{{ }}` (define variables), tags are `{% %}` (define logic and control flow), and filters are `{{ xyz | zyx }}` (filter output).

We need "front matter" in order for Jekyll to actually process Liquid. Front matter should go at the top of the html document. It is `yaml` with some specs in it. We use it to set variables for the page. Here is an example below: 

```html
---
this_number: 5
---
```

Front matter can be called in a page:

```html
---
title: Home
---
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>{{ page.title }}</title>
  </head>
  <body>
    <h1>{{ "Hello World!" | downcase }}</h1>
  </body>
</html>
```

Layouts are used to define defaults for certain types of pages. We can define a super basic one like this: 

```html
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>{{ page.title }}</title>
  </head>
  <body>
    {{ content }}
  </body>
</html>
```

And then the `index.html` page becomes:

```html
---
layout: default
title: Home
---
<h1>{{ "Hello World!" | downcase }}</h1>
```

`includes` helps with navigation. We define paths in the `_includes` folder and then use it in line in the actual `html` we produce.

`_data` allows for `yml` files to define navigation routes or hold any sort of `csv` or `yml` data.



## Resources

1. [Jekyll Tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/)
2. 

