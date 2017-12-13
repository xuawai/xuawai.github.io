---
layout: post
title: "Chapter 2 : The term vocabulary and postings lists"
description: ""
category: 
tags: []
---
{% include JB/setup %}

# 2.1 Document delineation and character sequence decoding
## 2.1.1 Obtaining the character sequence in a document
* convert the byte sequence into a linear sequence of characters(e.g., unicode to ASCII)  
&emsp;	* machine learning classification  
&emsp;	* heuristic methods  
&emsp;	* user selection  
&emsp;	* document metadata   
## 2.1.2 Choosing a document unit
* the issue of index granularity needs paying more attention  
# 2.2 Determining the vocabulary of terms   
## 2.2.1 Tokenization  
*token* : A token is an instance of a sequence of characters in some particular document that are grouped together as a useful semantic unit for processing  
*type* : A type is the class of all tokens containing the same character sequence  
*term* : A term is a (perhaps normalized) type that is included in the IR system’s dictionary  
**e.g.** >sleep perchance to dream  includes 5 tokens,4 types, 3 terms.  

