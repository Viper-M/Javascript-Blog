Though there are no must rules for writing javascript code but programmers should follow some rule to make the code readable to others.
Style -
Here some example of best practices given -
if (condition) {
// do this
// …and that
// …and that
}
A if condition should be written like this –
if (n < 0) {
alert(`Power ${n} is not supported`);
}
Horizontal line length should not to be so long as long line is disturbing to read.
The most important thing is function. A function can be written with so many variant. But best variant is look like this–
function style(x, n) {
let result = 1;
//
for (let i = 0; i < n; i++) {
result *= x;
}
//
return result;
}
The code and function calling should be ordered look like this –
let item = createItem();
setHandler(item);
walkAround();
// — — helper functions — -
function createItem() {
…
}
function setHandler(item) {
…
}
function walkAround() {
…
}
Semicolon placement is another important thing. Programmers should not skip the semicolon.
Comments –
Comments is one of the most important part of the code which makes the code readable and easy to understand. For this commenting on code is suggestible, but unnecessary and irrelevant comments is strongly prohibited.
The functions and method name should be meaningful.
addNumber(2, 3);
By this type of naming commenting can be reduced.
Cross browser performance –
As javascript is a web based language its main performance is measured on browser. For different types of browser it can be possible that the code perform differently. For why developers need to conscious about cross browser testing.
Testing on various browser and platform is called cross browser testing. A testing can be run by these steps -
Initial planning > Development > Testing/discovery > Fixes/iteration
After finding the result developers need to upgrade the code as needed.
ES6 Var Declaration –
Before es6 there were only var keyword for declare variable in javascript. But ES6 introduced with two brand new idea abou var declaration.
let number = 10;
let name = “Jhon”;
const number = 10;
const name  = “Jhon”
The main difference between this two is let variable is changeable by code but const variable is fixed value.
Hoisting -
ES6 is the latest version of ecmasript. This version made some upgradation on hoisting.
The first thing is that variables declared with let keyword are blocked scooped not function scooped.
let name;
console.log(name); // Output: undefined
name = 'Jhon'
The const variable value cannot be modified once assigned. But the hoisting system is same like as let variable.
const PI;
console.log(PI); // Ouput: SyntaxError: Missing initializer in const declaration
PI=3.142;
Block level declaration –
Which variables are inaccessible outside of given block scope is called block level declaration.
Block scope can be made –
1. Inside of a function
2. Inside of a block
Block bindings in loop -
On previous Ecmascript version we used var keyword to variable declaration. For that the variable declared on for loop was traceable after the loop ends.
for (var i=0; i < 10; i++) {
setItems(items[i]);
}
// i is still accessible here
console.log(i);
Now the let keyword of ES6 makes the difference. Assigning value by let is no more accessible after the loop ends.
for (let i=0; i < 10; i++) {
setItems(items[i]);
}
// i is not accessible here - throws an error
console.log(i);
Global Block Bindings –
Let and const has so many difference with var. One of them is their global scope behavior. Var is used in global scope, it can be traceable before the line it assigned.
But if we use let or const in the global scope, a new binding can be created but no property is added to the global object.
Spread Operator –
This spread operator […] is used to expand or spread an array.
const array = [‘My’, ‘name’, ‘is’, ‘John’];
console.log(array);
// [“My”, “name”, “is”, “Jack”]
console.log(…array);
// My name is Jack
This operator can use to copy the items into single array.
const arr1 = [‘one’, ‘two’];
const arr2 = […arr1, ‘three’, ‘four’, ‘five’];
console.log(arr2);
// Output:
// [“one”, “two”, “three”, “four”, “five”]
Arrow function –
One of the most useful feature in modern javascript is arrow function. It is also called fat arrow function. With very clean syntax its earn the popularity from programmers.
const add = (a, b) => a + b;
This format of function easy to implement and made code improved. This function can be use with multiple lines also.
(x, y) => {
let a = 1;
return a + x + y;
}
