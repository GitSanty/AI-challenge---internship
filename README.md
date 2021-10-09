# AI LAB CHALLENGE

# Context
Sensitive data has great value, which is why many governments have established regulations that address both data protection and data privacy. The General Data Protection Regulation (GDPR) of the European Union (EU) is one of the most influential laws in recent years. Any company that does business in theEU or the European Economic Area (EEA), or that markets products or services for people in the EU or EEA must  comply  with  GDPR  standards  or  face  severe  financial  repercussions  in  the  form  of  fines  and injunctions.

The  CMS.LawGDPR  Enforcement  Tracker  is  an  overview  of  fines  and  penalties  which  data  protection authorities within the EU have imposed under the EU GDPR. Different features are involved in this dataset(e.g., Id,  Country, Date  of decision,  Fine,  Controller/Processor, Quoted  Article,  Type,  Source,  Authority, Sector, and Summary). The Summary feature provides a free text description of the violation. It would be interesting  to  extract  patterns  from  such  descriptions  to  learn  from  these  examples,  and  thus  prevent companies from committing the same breaches.

# Description
In this challenge, we want to explore different natural language processing and text mining techniques to discover knowledge from the summaries of fines and penalties in the GDPR Enforcement Tracker dataset. The  goal  is  to cluster  the  descriptions  of GDPR  violationsand  also  discover  patterns  from  similar descriptions. 

# Tasks:

1.Test different textual representation models and preprocessing tasks 
2.Discover similar descriptions and characterize the obtained clusters
3.Discover patterns (e.g., topics) from the analyzed descriptions 
4.Visualize and validate the obtained results

# Requirements
• Input: summaries  of  GDPR  violations,  extracted  from  the GDPR  EnforcementTracker  dataset https://www.enforcementtracker.com/
• Output: obtained clusters and their characterization
• frameworks: for Natural Language Processing (NLP): NLTK and spaCy. For Machine Learning (ML): SciKit-learn and Keras



# Understanding NLP
Scientists have been working on this precise question since the turn of the last century and,
as of today, we have attained reasonable success in this area. The research on how to make
computers understand and manipulate natural languages draws from several fields,
including computer science, math, linguistics, and neuroscience, and the resulting
interdisciplinary area of research is called NLP. Take a look at the following diagram,
which illustrates this:

![image](https://user-images.githubusercontent.com/26960395/136666505-7b85b1ab-b706-453e-af31-422c894a6f7c.png)

 
# Getting a high-level overview of the spaCy library
spaCy is focused on production and shipping code, unlike its more academic 
predecessors. The most famous and frequently used Python predecessor is NLTK. NLTK's 
main focus was providing students and researchers an idea of language processing


![image](https://user-images.githubusercontent.com/26960395/136666641-34fa009b-efdc-40fe-bbc9-558af49834b1.png)


# Overview of spaCy conventions
When we call nlp on our text, spaCy applies some processing steps. The first step is 
tokenization to produce a Doc object. The Doc object is then processed further with a 
tagger, a parser, and an entity recognizer. This way of processing the text is called a 
language processing pipeline. Each pipeline component returns the processed Doc and 
then passes it to the next component:


![image](https://user-images.githubusercontent.com/26960395/136666795-9aa24dce-d81c-4a39-9768-72bc7dcb7c9c.png)


The Language class applies all of the preceding pipeline steps to your input sentence 
behind the scenes. After applying nlp to the sentence, the Doc object contains tokens that 
are tagged, lemmatized, and marked as entities if the token is an entity (we will go into 
detail about what are those and how it's done later). Each pipeline component has a welldefined task:


![image](https://user-images.githubusercontent.com/26960395/136666826-6f8f12fb-9007-4536-9256-03d431a701c2.png)

