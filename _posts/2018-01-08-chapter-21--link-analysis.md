---
layout: post
title: "Chapter 21 : Link analysis"
description: ""
category: NLP
tags: [notes on Introduction to information retrieval]
---
{% include JB/setup %}

# 21.1 The Web as a graph
### 21.1.1 Anchor text and the web graph
* The fact that the anchors of many hyperlinks pointing to `http://www.ibm.com` include the word `computer` can be exploited by web search engines, with a penalty for terms that occur very often (the most common terms in an- chor text across the Web are Click and here, using methods very similar to idf).  
* The use of anchor text has some interesting side-effects.**e.g.,** searching for big blue on most web search engines returns the home page of the IBM corporation as the top hit.   

# 21.2 PageRank
* The idea behind PageRank is that pages visited more often in this walk are more important.  
* **teleport:** In the teleport operation the surfer jumps from a node to any other node in the web graph.  
### 21.2.1 Markov chains
### 21.2.2 The PageRank computation
### 21.2.3 Topic-specific PageRank
* Suppose our random surfer, endowed with a teleport operation as before, teleports to a random web page `on the topic of sports` instead of teleporting `to a uniformly chosen random web page`.   

# 21.3 Hubs and Authorities
* We now develop a scheme in which, given a query, every web page is assigned two scores. One is called its `hub` score and the other its `authority` score.  
### 21.3.1 Choosing the subset of the Web
* Build the base set of pages, to include the root set as well as any page that either links to a page in the root set, or is linked to by a page in the root set.  
* **cross-language retrieval:** where a query in one language retrieves documents in another.   

