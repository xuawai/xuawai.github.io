---
layout: post
title: "Chapter 1 : Boolean retrieval"
description: ""
category: NLP
tags: [notes on Introduction to information retrieval]
---

*IR Definition：*Information retrieval (IR) is finding material (usually documents) of an unstructured nature (usually text) that satisfies an information need from within large collections (usually stored on computers).
# 1.1 An example information retrieval problem
* *grep* : linear scan through documents
* *incidence matrix term* :
![](/snapshot/1.png)
to query Brutus AND Caesar AND NOT Calpurnia:  110100 AND 110111 AND 101111 = 100100
* *ad hoc retrieval* : provide documents from within the collection that are relevant to an arbitrary user information need, communicated to the system by means of a one-off, user-initiated query   
&emsp;	* information need : what the user desires to know  
&emsp;	* query : what the user conveys to the computer for information need
* effectiveness evaluation methods: precision, recall. 
* *inverted index/inverted files* : 
![](/snapshot/2.png)
when the corpus is large, incidence matrix term is extremely sparse  
*posting* : each item in the list, which records that a term appeared in a document   
*postings list* : the list   
*postings* : all the posting list together 

# 1.2 A first take at building an inverted index
* procedure  
&emsp;	1. collect the documents;  
&emsp;	2. tokenize the text;  
&emsp;	3. produce normalized tokens;  
&emsp;	4. index the document;  
* something about storage  
&emsp;	* the dictionary(along with document frequency) is kept in memory;  
&emsp;	* the postings lists are kept on disk:  
&emsp;&emsp;* linked lists   
&emsp;&emsp;* variable length arrays.  
&emsp;&emsp;* hybird scheme with a linked list of fixed length arrays for each term  
* This inverted index structure is essentially without rivals as the most efficient structure for supporting ad hoc text search

# 1.3 Processing Boolean queries
* simple conjunctive query(AND)  
&emsp;	* solution : intersection
&emsp;	&emsp;	* when facing many terms(a AND b AND c), we process the query in increasing order of the size of each disjunctive term

# 1.4 The extended Boolean model versus ranked retrieval
* *free text queries* : type one or more words rather than using a precise language with operators for query expressions
* *proximity operator* : a way of specifying that two terms in a query must occur close to each other in a document




