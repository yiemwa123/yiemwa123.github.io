---
layout: page
title: Blog
---
* TOC
{:toc}

# Week 2

## Progress report:

For the second week, I worked on refining what I had completed last week. In the case the clue that the child provides is not an exact match to the information provided in ConceptNet, but similar in meaning, I was able to get the system to return a guess on an object with a property that is similar in meaning to the clue provided. I was also able to narrow down the list of properties of each entity extracted from and image by cutting out repetitive terms. I also found code provided by a past intern in the form of an Android app and looked to that as a reference point on how I could narrow down the search space.

## Some problems I encountered:


# Week 1

## Progress report:

For this first week, I mostly familiarized myself with what past interns have already worked on and coding a basic implementation of AISpy where the agent is the one guessing and the child provides the clue. I also took a look at different papers related to BERT and question-answer generation to see if there was anything I could work off of as well as different knowledge bases to see what useful information could be extracted to use during gameplay. By the end of the first week, the code I wrote was able to extract a keyword, assuming the child says the clue in the form "I spy something that is..." and query and process information on dummy data using the ConceptNet API. If there was a match between the clue and information extracted from ConceptNet, the agent would return the guess in the form of "Is it a \[object\]?" where the object is the entity with the property that matches the clue. I also got a simple implementation of a question in the form of "What is \[object\] \[relation\]?", where a relation was extracted from relevant relations from ConceptNet.

## Some problems I encountered:

The main problem that I encountered during this first week is run time, since it would take the system a while before it would be able to generate a guess. The issue was that I was querying on multiple different relations. However, I wasn't sure of the best way to narrow down which relations I was querying on. Another was that I was also trying to think of the types of clues a child might say, which made coding to account for all these different scenarios difficult. I also had a hard time understanding BERT and how to incorporate it into Q and A generation.
