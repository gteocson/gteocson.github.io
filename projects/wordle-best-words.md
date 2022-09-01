---
layout: project
type: project
image: img/wordle/wordle_app.jpg
title: "What Makes A Good Wordle Word"
date: 2014
published: true
labels:
  - Python
  - Jupyter Notebook
summary: "A small project for EE396 to find the best word and words to use"
---
<p align="center">
  <img width="500"
     src="../img/wordle/wordle_header.png">
</p>

# More Is Better

Wordle the 5-letter word guessing game that took the world by storm. During my EE396 course we explored what creates a good word. Though the challenge isn't about finding a good word it is about finding a good set of words. This non-static learning is exactly what the course is about. 

When you guess a word there may be a specific word that gives you the highest probability of information. However, after you guess that single word what is the best second guess. Depending on the pattern there may be multiple best choices. 

But how would you find that out? We explored the entropy of a word and the number of patterns associated with that word. To find the number of patterns with each word would use the function below. Note that our word bank isn't the same as wordles and I think they are still updating it as well.


`
dictionary = {}

for z in answers:

    dictionary.clear()
    
    for x in answers:
    
        p = getPattern(z,x)
    
        if p in dictionary.keys():

            dictionary[p]+= 1
        
        else:
        
            dictionary[p] = 1
    
    print("\nThe word is",z,"\nNumber of different patterns",len(dictionary))
`

# A New Project?

This small program was just an insight into information theory. In this specific course knowing about information theory is a good lead in into the larger project. More information about the project will be discussed in the module about the Huligutta game. 

Just for some information we beginning to work on machine learning and neural network related topics. Being able to recognize patterns and dynamically changing ones at that really showcases the beauty of AI and how we can code programs to learn so much faster than what a human can.


