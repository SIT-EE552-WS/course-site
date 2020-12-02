---
title: Enums that Behave Themselves
week: 6
homework: 5
---

Enums in Java are typically used to represent a set of related constants in a type-safe way.  For example, you might have something like

```java
enum DayOfWeek{
  SUNDAY,
  MONDAY,
  TUESDAY,
  WEDNESDAY,
  THURSDAY,
  FRIDAY,
  SATURDAY
}
```

But, as we saw in class, Java enums are more than just fancy variables.  They are full classes and can have behavior.  Create an named `Operation` with four values: `ADD`, `SUBTRACT`, `MULTIPLY`, `DIVIDE`.  Each one should have a property called symbol set to `+`, `-`, `⨉`, and `÷` respectively and should implement the method `int apply(int a, int b)` appropriately for the given operation.  The enum should also include a method `public Operation fromSymbol(char symbol)` that returns the appropriate enum value.
