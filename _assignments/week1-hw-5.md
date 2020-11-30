---
title: Drawing Grids
week: 1
homework: 5
---
Write a Processing program to create a 600x400 window and then draw
horizontal and vertical lines to divide the window into an evenly
spaced grid.  Your program should rely on a variable `n` such that
each the grid is made up of _n_ vertical and _n_ horizontal rectangles.
 For example, if `n=3`, your program should draw four lines to divide
 the window into nine squares like this.

 {::nomarkdown}
<svg width="600" height=400>
  <rect width="600" height="400" fill="#efefef" />
  <polyline points="0,133.3333333 600,133.3333333" stroke="black" stroke-width="2px"/>
  <polyline points="200,0 200,400" stroke="black" stroke-width="2px"/>
  <polyline points="0,266.6666666 600,266.3333333" stroke="black" stroke-width="2px"/>
  <polyline points="400,0 400,400" stroke="black" stroke-width="2px"/>
</svg>
{:/}
