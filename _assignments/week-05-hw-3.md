---
title: Bag of Words
week: 5
homework: 3
---

Although computers tend to read passages of text one word at a time, it can be 
advantageous for computers to process text as a "Bag of Words".  A Bag of Words 
is a representation of the text as a table of the unique words in the text and the 
number of times the word appears in the text.

Using a Bag of Words the following text:

```
This is Spot. See Spot run. Run, Spot, Run.
```

Would be represented like this (ignoring capitalization for the time being):

```
this    1
is      1
spot    3
see     1
run     3
```

Create a Bag of Words from the sample text provided with the assignment.  Use a `Map<String, Integer>` to store the result. Note: in the version of Java we're using there are many different ways to create this map.  We will look at some of the newer ways to do this in a later week.  For now, please limit your solution to only use the `put()` and `get()` methods of the `Map` class.
