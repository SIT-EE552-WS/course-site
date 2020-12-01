---
title: Fraction Math
week: 3
homework: 4
---

Last week, we covered some of the limitations of floating point numbers, 
but even if we aren't working in binary, there are many rational numbers 
that cannot be represented in decimal notation either, such as 1/3.

In the starter project, a class called `Fraction` has been provided with
stubs for various arithmetic operations.  Write the bodies of these methods 
so that they each return a new fraction with the correct value.  The fractions 
returned should be reduced to lowest terms.

For this assignment, you will need to consider some number theory concepts such as
Greatest Common Denominator (GCD) and Least Common Multiple (LCM).  The simplest way 
to find the GCD is with Euclid's Algorithm written in pseudocode as follows.

```
function gcd(a, b)
    while b ≠ 0
        t := b
        b := a mod b
        a := t
    return a
```    
