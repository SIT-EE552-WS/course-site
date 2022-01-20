---
title: Penner's Easing Functions
week: 3
homework: 1
source: Inspired by https://sighack.com/post/easing-functions-in-processing
---

In 2002 Robert Penner, who would go on to work for Adobe on the team developing Flash, 
wrote a book on computer animation in Flash.  In one chapter of his book, he described 
the concept of "Tweening" and "Easing".  In the days of traditional animation, Tweening
referred to the work done by more junior animators to draw out the individual frames 
be**tween** the keyframes drawn by a more senior animator.  In computer animation, tweening 
works much the same way, but the computers are using math to interpolate what these intermediary 
frames should look like.

We can think of animated motion as treating position as a function of time.  From physics, for 
linear motion, we have the equation $$ x = v t + x_0 $$.  But objects in the real world don't 
generally have constant acceleration.  It will take some time for a parked car to reach highway 
speeds when the driver puts their foot on the pedal.  In his book, Penner described a series of 
"easing" functions that allowed for more dynamic position functions such as "easing in", the object
slowly accelerates to a constant speed, "easing out", the object starts fast and slows down towards 
the end of its path, and several others.  These functions have become standards today in many 
computer animationtools.

Each of the equations takes the following form:

```
getTweenPosition (time, begin, change, duration) {
  // calculate position here
  return position;
};
```

Because they all have this same form, we can model them as simple objects and rely on polymorphism 
to use them.  In the starter project provided with this assignment, three of the easing functions have 
been implemented as classes.  Your task is to implement 7 other functions of your choice.  Try to name your 
classes intuitively.  The full list of equations can be found <a href="https://gist.github.com/aelfric/cf4ff52ba7eacc014278347da8c008be">here</a>.

To make it easier to visualize the easing functions, the first three have been rendered as a monochrome gradient with 
three equal vertical stripes, one for each easing function.  Create an gradient like this with 10 equal stripes, one for each easing function.
