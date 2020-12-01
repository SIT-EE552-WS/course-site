---
title: A Simple Spellchecker
week: 4
homework: 3
---

There are over 200,000 words in the English language with more being invented all the 
time. For various historical reasons, English has many complicated spelling rules for writing 
many of these words.  Modern spellcheckers like the one built into Micorosft Office use many language
processing techniques to provide the user with useful suggestions.

A simple spellchecker, though, can be written by checking each word against a list of all known words.  
Your task is to write a simple spellchecker in this way.  For simplicity's sake, your spellchecker will 
not need to learn all 200,000+ words of the language.  The starter project includes four text files:

* `words.txt` - a subset of the most common words in the language.
* `peter-pan.txt` - a short passage from the the book _Peter Pan_
* `alice.txt` - a short passage from the the book _Alice's Adventures in Wonderland_
* `original.txt` - an empty file that you should fill in with some text of your own writing.  Include some intentional misspellings.

Your task is to fill in the the method bodies in the starter project so that the program loads the words file 
and each of the sample texts and outputs the original text with each misspelling surrounded with two square brackets like this:

```
The [[qcuik]] brown fox jumped over the [[laazy]] dog
```
