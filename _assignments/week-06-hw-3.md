---
title: Equals and Hash Code
week: 6
homework: 3
---

A point in 3D space can be represented by Cateesian coordinates (x,y,z).  The same point can also be specified in Cylindrical coordinates (r,θ,z).  
You can check if two points in Cartesian space are equal by checking that each component matche.  You can do the same for two points in Cylindrical 
coordinates.  In order to compare a point in Cartesian coordinates to a point in Cylindrical coordinates, you will need to do some conversion.

In the starter project, three classes are defined `abstract 3DPoint` and two subclasses `CartesianPoint` and `CylindricalPoint`.  Implement `equals` 
and `hashCode` in both subclasses so that it is possible to test equality of points in both systems against each other.  The equations for converting 
between Cartesian and Cylindrical coordinates are:

\\[ x = r \cos \theta \\]

\\[ y = r \sin \theta \\]

\\[ z = z \\]

Remember, the Java trigonometric functions use the `double` type which means you will need to account for possible rounding errors when checking equality.

Remember also, the Java library expects `hashCode` to behave like this:

* Whenever it is invoked on the same object more than once during an execution of a Java application, the hashCode method must consistently return the same integer, provided no information used in equals comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
* If two objects are equal according to the equals(Object) method, then calling the hashCode method on each of the two objects must produce the same integer result.
* It is not required that if two objects are unequal according to the equals(java.lang.Object) method, then calling the hashCode method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.
