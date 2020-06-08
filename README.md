# relaxer-app

<strong>Source:</strong>

Traversy Media<br>
Breathe & Relax App - JavaScript & CSS Animations<br>
https://www.youtube.com/watch?v=l-1ZrU6avzI<br>
https://github.com/bradtraversy/vanillawebprojects/tree/master/relaxer-app<br>

<strong>Known issue:</strong>

In Firefox, the CSS function "conic-gradient" is not supported.<br>
Using "svg" as fallback for the outer-circle, with a lower z-index, so that it's hidden in browsers where "conic-gradient" is supported.<br>
Calculations below adapted from:<br>
https://codepen.io/xgad/post/svg-radial-progress-meters<br>

C (circumference) = 2 * π * R<br>
R = 115<br>
C ~= 722.5663<br>

dasharray for the "breathein" and "breatheout" circles:<br>
1st value = dash = 2/5 * C = 289.0265<br>
2nd value = gap = C = 722.5663<br>

dashoffset (negative) for the "breatheout" circle:<br>
offset = -3/5 * C = -433.5397<br>

dasharray for the "hold" circle:<br>
1st value = dash = 1/5 * C = 144.5132<br>
2nd value = gap = C = 722.5663<br>

dashoffset (negative) for the "hold" circle:<br>
offset = -2/5 * C = -289.0265<br>
