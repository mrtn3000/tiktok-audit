---
layout: post
title: documenting your data
date: 2023-08-01 15:09:00
description: an example of a blog post with some code
tags: code
categories: how-to
featured: false
---
# Documenting your data

So you've set up some scrapers to gather data from the platform you are auditing and are now swimming in it. But what exactly are you gathering?

In this notebook, we explore a strategy to create a codebook template to make the process of documenting your data easier. We assume you have been working a Mongo-like database with collections that store JSON documents.

We will be using [`GenSON`](https://github.com/wolverdude/genson/), a "powerful, user-friendly JSON Schema generator built in Python". Read the library's documentation for more information.

## The problem

You want to document your data because knowing what you have is the very first step in gaining insights from it. In the ideal scenario, all documents are composed of the same variables and only vary in content. However, you will most likely have documents with varying structures; this is specially true if you have collected data from different sources and along a longer timespan. The structure of a document is sometimes referred to as a *schema*, although other -potentially confusing- acceptations of this term exist. Think of a schema as a list of the variables a document contains; more sophisticated schemas could also specify variable types. Also, if a document contains a nested structure of variables, its schema should also reflect that.

Consider a collection with documents A and B. Say document A contains values for 5 variables and document B includes 4 of them. If all of B's variables are contained in A, then all we have to do to produce a thorough schema of our collection is to generate the one corresponding to A. But what if the contents of A and B don't overlap? Or if they do so only partially? Since we want to take note of *every single variable* we are collecting, we would want all of the variables contained in A and B, while making sure we don't include those in both twice. This is the equivalent of the union of both sets, if you are familiar with basic set theory.

So, in order to create a thorough global schema for a collection of documents, we need to consider each of its individual document schemas. This is in fact as daunting as it sounds, as collections created by tasks like automated web scraping are usually composed hundreds of thousands of documents. Fortunately, there is an open-source tool at our disposal which can be used for this very purpose.

Enter `GenSON`....

## Using `GenSON` to generate schemas

The problem we face comes up quite often in database management, albeit in a different avatar. We are not going into the details here, but suffice it to say that `GenSON` is a library used for schema validation purposes; you can read more about it [here](https://json-schema.org/draft/2020-12/json-schema-validation.html). The library offers a set of tools that allow us to consider several documents -in JSON format- at the same time in order to *infer* the corresponding sglobal schema that considers *every single variable* in *every single document*, hence producing a thorough schema.

The basic workflow is to instantiate a `SchemaBuilder` object, and then add the documents from which we want to infer the schema to it. You may require some wrangling to feed your builder valid JSON objects. This can be accomplished by using some functions includded in the `json` module, part of the Standard Python Library. Here is a snippet you can youse as an outline:


```py
import json
from genson import SchemaBuilder

builder = SchemaBuilder()
for document in sample:
    document = json_util.dumps(document)
    document = json.loads(document)
    builder.add_object(document)
schema = builder.to_schema()
```

**To be continued...**
