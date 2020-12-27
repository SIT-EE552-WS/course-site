---
title: The Strategy Pattern with Lambdas
week: 12
homework: 4
---

In assignment 6.5, we created an Operator enum and used method overriding to implement each operator.  Now, lambdas
give us another way to express the same behavior.  Create a new version of the `Operator` enum that has the same behavior
but instead of using a method override, give each instance of the enum a property called `operation` of type `BiFunction<Integer, Integer, Integer>` 
that is initialized in the constructor of each enum instance.  Write labmda functions to implement the four basic arithmetic operations.
