---
layout: post
title: "Chapter 2 : The term vocabulary and postings lists"
description: ""
category: 
tags: []
---
{% include JB/setup %}

# 2.1 Document delineation and character sequence decoding
### 2.1.1 Obtaining the character sequence in a document
* convert the byte sequence into a linear sequence of characters(e.g., unicode to ASCII)  
&emsp;	* machine learning classification  
&emsp;	* heuristic methods  
&emsp;	* user selection  
&emsp;	* document metadata  

### 2.1.2 Choosing a document unit
* the issue of index granularity needs paying more attention  

# 2.2 Determining the vocabulary of terms
   
### 2.2.1 Tokenization  
*token* : A token is an instance of a sequence of characters in some particular document that are grouped together as a useful semantic unit for processing  
*type* : A type is the class of all tokens containing the same character sequence  
*term* : A term is a (perhaps normalized) type that is included in the IR system’s dictionary  
**e.g.** `to sleep perchance to dream`includes 5 tokens,4 types, 3 terms.    
*language identification* : identifier language based on classifiers  
* one solution is to encourage users to input over-eager and search for 'over-eager' or 'over eager' or 'over eager'  
&emsp;	* hyphenation : hyphens needs paying attention  
&emsp;	* white space : sometimes white space splits what should be regarded as a single token
  
### 2.2.2 Dropping common terms: stop words  
*stop words* some common words which are of little value in helping select documents    
* some stop words may be useful, **e.g.**,`flights to London` means nothing without `to`   
* modern IR systems tend to ignore stop words gradually
  
### 2.2.3 Normalization (equivalence classing of terms) 
*token normalization* : canonicalize tokens so that matches occur despite superficial differences in the character sequences of the tokens  
*equivalence classes* : different format of the same token
* maintain a query expansion list of multiple vocabulary entries for a certain query term  
* perform the expansion during index construction, e.g., index `automobile` under `car` as well  
* commonly employed normalization  
&emsp; 1. Accents and diacritics  
&emsp; 2. Capitalization/case-folding(*truecasing* : uses more features to make the decision of when to case-fold)  
&emsp; 3. Other issues in English  
&emsp; 4. Other languages




