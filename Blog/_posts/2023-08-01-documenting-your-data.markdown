---
layout: post
title: documenting your data
date: 2023-08-01 15:09:00
description: an example of a blog post with some code
tags: code
categories: how-to
featured: true
---
**Documenting your data**

So you've set up some scrapers to gather data from the platform you are auditing and are now swimming in it. But what exactly are you gathering?

In this notebook, we explore a strategy to create a codebok template to make the process of documenting your data easier. We assume you have been a Mongo database witha collection that stores JSON documents.

We will be using [`GenSON`](https://github.com/wolverdude/genson/), a "powerful, user-friendly JSON Schema generator built in Python". Read the library's documentation for more information.

**The problem**

You want to document your data. In the ideal scenario, all documets are composed of the same variables and only vary in content. However, you have documents of varying sizes and contents. Which document should you use as prototype to create your code book? The largest is a natural guess, but some smaller document may contain variables not present in the largest one.

Enter `GenSON`.

```py
builder = SchemaBuilder()
for document in sample:
    document = json_util.dumps(document)
    document = json.loads(document)
    builder.add_object(document)
schema = builder.to_schema()
```

**To be continued...**

