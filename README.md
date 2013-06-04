
# Objective-J Acorn

A tiny, fast JavaScript and Objective-J parser with built in preprocessor. Written in JavaScript.

It is extended from the Acorn JavaScript parser by Marijn Haverbeke:

See http://marijnhaverbeke.nl/acorn/

It is 100% compatable with JavaScript with two extra options.

1: Turn on 'preprocess' to allow C like preprocess derectives.

Example:
```c
#define MAX(x, y) (x > y ? x : y)
var m1 = MAX(a, b);
var m2 = MAX(14, 20);
```
Will be parsed as if it was like this:
```c
var m1 = (a > b ? a : b);
var m2 = (14 > 20 ? 14 : 20);
```
For more info see http://www.cappuccino-project.org/blog/2013/05/the-new-objective-j-2-0-compiler.html

2: Turn on 'objj' to allow Objective-J syntax

See http://www.cappuccino-project.org/learn/objective-j.html
