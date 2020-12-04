---
title: Producers / Consumers
week: 13
homework: 5
---

Write a program that creates two threads.  In one thread is a Producer that generates numbers sequentially counting by fives that places 
a number into a queue once per second.  The queue can only hold 10 items.

In the other thread is a Consumer that reads two numbers from the queue every five seconds.  It should print the two numbers retrieved from 
the queue to the screen.
