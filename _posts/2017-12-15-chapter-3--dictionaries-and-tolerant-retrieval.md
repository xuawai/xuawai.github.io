---
layout: post
title: "Chapter 3 : Dictionaries and tolerant retrieval"
description: ""
category: NLP
tags: [notes on Introduction to information retrieval]
---
{% include JB/setup %}

# 3.1 Search structures for dictionaries
* Two solutions for dictionaries : hashing, and search trees.  
* Hash   
There is no easy way to find minor variants of a query term , since these could be hashed to very different integers;
In a setting where the vocabulary size keeps growing, a hash function designed for current needs may not suffice in a few years’ time.  
*Search tree : binary tree, B-tree  

# 3.2 Wildcard queries
* Using a regular B-tree(e.g., for `mon*`) together with a reverse B-tree(e.g., for `*mon`), we can handle an even more general case, e.g., `se*mon`  

### 3.2.1 General wildcard queries
#### Permuterm indexes
![refer to figure 3.3](../snapshot/5.png)
* e.g., when the query is `fi*mo*er`, we first enumerate the terms inn the permuterm index of `er$fi*`, then filter out what doesn't have the string `mo` in the middle.  
* Disadvantage: the dictionary is quite large.  

### 3.2.2 k-gram indexes for wildcard queries

