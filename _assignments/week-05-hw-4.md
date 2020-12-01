---
title: Text Summarization
week: 5
homework: 4
---

**NOTE 1**: The solution to this assignment depends on the solution to homework 5.3, 
Please be sure that your solution to that assignment works before copying any code 
into your solution for this assignment.

**NOTE 2**: There are only four assignments this week instead of five because 
this assignment is a bit more involved than the ones for previous weeks.  Please
plan your time accordingly.


## Part 1 - Cosine Similarity ##

Thinking back to geometry and linear algebra, a normalized vector quantity represents a direction.  Two vectors can be said to be similar 
if the angle between the vectors is very small (If the angle is 0 degrees, they are equal, if the angle is 180 degrees they are exact opposites).
It is possible to determine the angle between two vectors by using the Euclidean dot product formula.
 
$$ A \cdot B = ||A|| ||B|| \cos(\theta)$$
 
Therefore,
 
$$ \cos(\theta)  = \frac{||A|| ||B||}{A \cdot B }$$
 
We don't really need the angle - using the cosine of the angle is good enough.  A value of 1 means the two vectors are identical.  
A value of -1 means the vectors could not be more different.

**Write a method to calculate the cosime similarity of two vectors **

## Part 1: Term Frequency Vectors ##

In homework 5.3, we constructed a Bag of Words (BoW) from a text package. Bag of Words representations
are used for many applications in natural language processing (NLP).  We can take the BoW
and turn it to a vector (i.e. the type you'd find in linear algebra).  So, for our example text, 
`This is Spot. See Spot run. Run, Spot, Run.` which had the following BoW representation:

```
this    1
is      1
spot    3
see     1
run     3
```

we might represent this as the vector `[1, 1, 3, 1, 3]`, or, if we normalize the vector based on the 
number of words in the original text `[1/5, 1/5, 3/5, 1/5, 3/5] = [0.2, 0.2, 0.6, 0.2, 0.6]`.  
Each element in the vector represents the frequency of a term in the original text.  To know which term
each element represents, you would need to look back at our original table.

Now let's say we wanted to compare our example text with another text: `This is Jane. See Spot run to Jane.`, which would 
have the following BoW:
```
this    1
is      1
jane    2
spot    1
see     1
run     1
```

We can make that a vector `[1/6, 1/6, 2/6, 1/6, 1/6, 1/6] = [0.16666..., 0.16666..., 0.33333..., 0.16666..., 0.16666..., 0.16666...]`, 
but we can't do any operations on the pair vectors because they have different legnths. (Even if the vectors 
were the same length, we really couldn't do any meaningful operations on the vectors because the elements 
map to different words.  In the frist vector, the frequency of the word `spot` is represented by the third 
element, but in the second vector it's represented by the fourth.)

So instead, we want to map both sentences to the same vector space including zeroes for words that appear in one sentence but
not the other:
```
       s1    s2
------------------
this    1     1
is      1     1
jane    0     3
spot    3     1
see     1     1
run     3     1
```

Or with normalizing (each sentence is still normalized using only the number of words in the original sentences, not the total number of words)

```
        s1      s2
--------------------------
this    0.2     0.16666...
is      0.2     0.16666...
jane    0.0     0.33333...
spot    0.6     0.16666...
see     0.2     0.16666...
run     0.6     0.16666...
```

**Given a list of sentences, create the normalized term frequency vectors for 
each sentence using the combined vocabulary as shown in the example above**.  

## Part 3 - Inverse Document Frequency ##

When searching for something, you generally want to focus on the characteristics that makes it unique.  If you're looking
for a book on your shelf, your first thought probably isn't "It has white pages".  Likewise, in English, if you try to 
find all the sentences in this homework that contain the word "the", you might as well just look at every sentence.  
The Inverse Document Frequency is a statistical measure used to represent how important or unique a word is. The formula is:

$$ IDF(t) = \log \frac{N}{df_t} $$

Where $$N$$ is the total number of documents and $$df_t$$ is the number of documents that contain the term $$t$$.  Note that
for our purposes, a "document" is actually a sentence.  

Similar to term frequency, we can createa a vector of IDF values for each word.

```
        IDF
--------------------------
this    0.0
is      0.0
jane    0.30102...
spot    0.0
see     0.0
run     0.0
```

"Jane" is the only word with a positive value, because it is the only word that is in one sentence but not the other.

**The second part of the assignment is, given a list of sentences, create the IDF vector for the combined list of words in each sentence.**

## Part 4 - Text Summarization ##

We're all busy.  Who has time to read anymore?  Imagine if you could take a long article and automatically identify only the most 
important sentences in the article.  While there are certainly ways to create something a bit, we are going to make a simple summarizer
by combining the work we did in Parts 1,  2, and 3.

A term frequency–inverse document frequency (TF-IDF) vector is made by multiplying (dot product) the TF vector from Part 1 
with the IDF vector in Part 2.  This is another metric on how important each word is to the source text.  
A rare word (high IDF) that appears multiple times (high TF) is more important than a common word (low IDF) that appears few times (low TF).  
By feeding two TF-IDF vectors into the Cosine Similarity function from Part 1, we can generate a scalar value representing how similar the 
two sentences are.

So one way to summarize the long text is to eliminate as much repetition as possible. We want to select the sentences 
that have the most overlap with other sentences in the article.

**For each sentence in the longer text, calculate the TF-IDF vector for the sentence and then calculate the cosine 
similarity between that sentence's vector and every other sentence's vector.  Finally, select the sentences that 
have the highest average similarity measure and output them in the proper order to a file called `summary.txt`.  
Some helper methods are already provided in the project scaffold.**

 *One more note:* English is a messy language.  In the project folder are two files `original.txt` and `clean.txt`
