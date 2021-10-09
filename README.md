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

