---
title: Simple Calculator
week: 13
homework: 1
---

In the starter project, a screen for a simple calculator has already been created for you.  Each button is connected to a handler method.  You can look at the `calculator.fxml` file to see which methods handle which buttons.  Your job is to make the calculator work for basic arithmetic.

The simplest calculator uses three registers:
* The current number being displayed
* The current operation being performed
* The previous number in memory

When you hit a number key, the screen is updated.  When you hit an operator, the displayed number is moved to memory, the display is cleared, 
and the current operator is set. When the equals button is pressed, the operator is applied to the previous number in memory and the current number 
on the screen and the screen is updated with the result.

Create some fields in the `CalculatorController` class to represent these concepts.  For the operator, you may want 
to reuse the Operator enum you made in a previous assignment.  Then implement the button handler methods accordingly.
