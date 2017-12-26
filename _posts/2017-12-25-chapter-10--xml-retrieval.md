---
layout: post
title: "Chapter 10 : XML retrieval"
description: ""
category: NLP
tags: [notes on Introduction to information retrieval]
---
{% include JB/setup %}

* **structured retrieval:** Many structured data sources containing text are best modeled as structured documents rather than relational data.  
* **structured retrieval** and **semistructured retrieval** both refer to XML retrieval.  


# 10.1 Basic XML concepts
# 10.2 Challenges in XML retrieval
1.Users want us to return parts of documents (i.e., XML elements), not entire documents.  
&emsp; * **Structured document retrieval principle:**A system should always retrieve the most specific part of a document answering the query.  
2.Which parts of a document to index.
&emsp; * **extended queries:**Interpreting all parent-child relationships in queries as descendant relationships with any number of intervening nodes allowed.   

# 10.3 A vector space model for XML retrieval
* **lexicalized subtrees：**subtrees that contain at least one vocabulary term.  
* The main difference is that the dimensions of vector space in unstructured retrieval are vocabulary terms whereas they are lexicalized subtrees in XML retrieval.  
`skipped for now` for some algorithms  

# 10.4 Evaluation of XML retrieval
* **INEX (INitiative for the Evaluation of XML retrieval) program:** a collaborative effort that has pro- duced reference collections, sets of queries, and relevance judgments.  
* INEX 2002 defined component coverage and topical relevance as orthogonal dimensions of relevance.   
&emsp; 1.The component coverage dimension evaluates whether the element retrieved is “structurally” correct, i.e., neither too low nor too high in the tree.  
&emsp; 2.The topical relevance dimension also has four levels: highly relevant (3), fairly relevant (2), marginally relevant (1) and nonrelevant (0).   

# 10.5 Text-centric vs. data-centric XML retrieval
* **Text-centric：** We match the text of the query with the text of the XML documents.  
* **Data-centric:** Data-centric XML mainly encodes numerical and non-text attribute-value data.  
* There are powerful query languages for XML that can handle numerical attributes, joins and ordering constraints. The best known of these is XQuery.  
