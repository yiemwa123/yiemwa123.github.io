---
layout: default
title: Blog
---

## Week 10

### Progress report:

For this week, I incorporated Flask into the Android app and worked on reducing the amount of filtering needed to be done for when the agent makes a guess in order for the app to not be bogged down by runtime. I also figured out a way to test other images without using an Android device.

### Some problems I encountered:
The main issue was that the long run time for the QA generation caused the app to crash, so we decided to reduce the amount of text that was being used to generate QA pairs.

## Week 9

### Progress report:

I continued working on integrating the Python code into the Java code and supporting the ranking system in the Android app. I was also trying to look for ways to test other images besides the default image in the Android emulator. I also tried to explore ways to support a backend into the app to better integrate QA generation.

### Some problems I encountered:
The main issue was that it was difficult to test on a different set of images.


## Week 8

### Progress report:

I worked on filtering text for the QA pipeline so we could filter out words that may be too difficult for 3-5 year olds to understand. I was also able to successfully integrate Chaquopy into the Android app.

### Some problems I encountered:
Since Java and Python sometimes have different types, it was sometimes hard to send information from Java and have it run in Python and I had to modify my code a lot to account for this.

## Week 7

### Progress report:

I worked on integrating my code into the Android app and tried to look into ways to integrate a Python question-answer generation model into an Android app. I ended up settling on Chaquopy, which is a Python SDK for Android. I also looked into potential ways that we could store information locally and worked more on the ranking algorithm for guesses.

### Some problems I encountered:
I had a hard time debugging Chaquopy, since Google Voice on the Android emulator does not pick up my voice very well, so I had to find ways to modify the code to allow me to give an input without using voice.

## Week 6

### Progress report:

I implemented interaction for when the agent is the spy and when the agent is the one providing the clue. Also tried to implementing some ideas of how to handle an interaction to allow the agent the "fail gracefully" so that even though the agent is not able to make a good guess, it can still be a valuable learning experience for the child. This week was also when I started to think of ways to improve upon ways the agent can give a guess or provide a clue.

### Some problems I encountered:
Most of the problems I encountered this week were related to how we wanted to program interactions where the agent is unable to provide a useful clue or an educated guess. We had to make a lot of assumptions as to what might be engaging for a child.

## Week 5

### Progress report:

I continued trying to code different interactions and was able to produce a basic command line version of the game and trying to improve that by implementing a ranking system for guesses. I also continued trying to play around with the question-answer generation and looking into other potential datasets that I could use.

### Some problems I encountered:
Not too many problems arose this week other than with training the model.

## Week 4

### Progress report:

This week was continuing the work that I built off of the week before and also taking a look at other resources. I also coded a potential interaction scenario and tried to incorporate new ideas for interaction design (e.g. ask the user for a synonym rather than having the agent figure out if the clue provided is similar to the properties provided by ConceptNet).

### Some problems I encountered:
The most trouble I had came from trying to train the model on a different dataset. It would not read the file, or I would get errors.

## Week 3

### Progress report:

For the third week, I worked on having the speech agent provide a guess to a clue provided by the child. To allow more flexibility in the clue the child provides, I worked on being able to allow the agent to provide an accurate guess, even if the clue provided is not an exact match to one of the properties returned from ConceptNet. I also worked question-answer generation models and tried using a Simple Wikipedia article to see what kinds of question answer pairs it produces.

### Some problems I encountered:
The main issues that I encountered this week had to do with long runtime due to filtering and trying to detect similarity between the clue and the words being returned by ConceptNet. I also ran into some issues with training the model because I don't have a GPU and I kept getting errors.


## Week 2

### Progress report:

For the second week, I worked on refining what I had completed last week. In the case the clue that the child provides is not an exact match to the information provided in ConceptNet, but similar in meaning, I was able to get the system to return a guess on an object with a property that is similar in meaning to the clue provided. I was also able to narrow down the list of properties of each entity extracted from and image by cutting out repetitive terms. I also found code provided by a past intern in the form of an Android app and looked to that as a reference point on how I could narrow down the search space.

### Some problems I encountered:
I was trying to figure out the most effective way to extract information from the user utterance and how I could utilize the NLP APIs. I was also concerned about potential issues with runtime and I had a difficult time understanding how NLP models generate QA pairs.



## Week 1

### Progress report:

For this first week, I mostly familiarized myself with what past interns have already worked on and coding a basic implementation of AISpy where the agent is the one guessing and the child provides the clue. I also took a look at different papers related to BERT and question-answer generation to see if there was anything I could work off of as well as different knowledge bases to see what useful information could be extracted to use during gameplay. By the end of the first week, the code I wrote was able to extract a keyword, assuming the child says the clue in the form "I spy something that is..." and query and process information on dummy data using the ConceptNet API. If there was a match between the clue and information extracted from ConceptNet, the agent would return the guess in the form of "Is it a \[object\]?" where the object is the entity with the property that matches the clue. I also got a simple implementation of a question in the form of "What is \[object\] \[relation\]?", where a relation was extracted from relevant relations from ConceptNet.

### Some problems I encountered:

The main problem that I encountered during this first week is run time, since it would take the system a while before it would be able to generate a guess. The issue was that I was querying on multiple different relations. However, I wasn't sure of the best way to narrow down which relations I was querying on. Another was that I was also trying to think of the types of clues a child might say, which made coding to account for all these different scenarios difficult. I also had a hard time understanding BERT and how to incorporate it into Q and A generation.
