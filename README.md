# uplab

____
# Задание 1
This code does not execute properly. Try to figure out why.(Multiply)
# Код
```html
function multiply(a, b){
  return a * b
}
```
____
# Задание 2
Given the triangle of consecutive odd numbers(Sum of odd numbers)
```html
function rowSumOddNumbers(n) {
  //TODO 
  return n*n*n
}
```
____
# Задание 3
Given an array of integers, find the one that appears an odd number of times.
There will always be only one integer that appears an odd number of times.(Find the odd int)
```html
function findOdd(A) {
  //happy coding!
  let odd;
  const counter = {};
A.forEach((num)=>{
  if (counter[num]) {
    counter[num]++;
  }
  else{
    counter[num] = 1;
  }
});
  for (let num in counter){
    if (counter[num] % 2 === 1){
      odd = num;
    }
  }
  return Number(odd);
}
```
____
# Задание 4
Check to see if a string has the same amount of 'x's and 'o's. The method must return a boolean and be case insensitive. The string can contain any char.(Exes and Ohs)
```html
function XO(str) {
    //code here
    str = str.toLowerCase();
    var string = str.split("");
    var X = string.reduce( function( n, val ) {
        return n + (val === 'x');
    }, 0);
    var O = string.reduce( function( n, val ) {
        return n + (val === 'o');
      }, 0);
    if ( X == O ) {
      return true;
    } else {
      return false;
    }
}
```
____
# Задание 5
Write a function that will return the count of distinct case-insensitive alphabetic characters and numeric digits that occur more than once in the input string. The input string can be assumed to contain only alphabets (both uppercase and lowercase) and numeric digits.(Counting Duplicates)
```html
function duplicateCount(text){
  //...
   let t = text.toLowerCase();
   let s = new Set();
   let d = new Set();
   for (let c of t) {
     if (s.has(c)) d.add(c);
     s.add(c);
  }
   return d.size;
}
```
____
# Задание 6
Implement a function that adds two numbers together and returns their sum in binary. The conversion can be done before, or after the addition.
The binary number returned should be a string. (Binary Addition)
```html
function addBinary(a,b) {
var sum = a + b,
  		binary = '';
  while ( sum > 0 ) {
    binary = ( sum % 2 ) + binary;
    sum = Math.floor( sum / 2 );
  }
  return binary;
}
```
____
# Задание 7
Complete the findNextSquare method that finds the next integral perfect square after the one passed as a parameter. Recall that an integral perfect square is an integer n such that sqrt(n) is also an integer.(Find the next perfect square!)

If the parameter is itself not a perfect square then -1 should be returned. You may assume the parameter is non-negative.(Find the next perfect square)
```html
function findNextSquare(sq) {
  // Return the next square if sq is a perfect square, -1 otherwise
 var x;
    var nextx;
    if(Math.sqrt(sq)%1 ===0){
         x=Math.sqrt(sq)
         nextx=x+1
    }else{
        return -1;
    }
    return nextx*nextx;
}
```
____
# Задание 8
Implement the function unique_in_order which takes as argument a sequence and returns a list of items without any elements with the same value next to each other and preserving the original order of elements.(Unique In Order)
```html
var uniqueInOrder=function(iterable){
  //your code here - remember iterable can be a string or an array
var X = [];
  for(var i = 0 ; i<iterable.length ; i++){
    if(iterable[i] !=iterable[i+1]){
      X.push(iterable[i])
    }
  }
  return X
```
____
# Задание 9
Given an array (arr) as an argument complete the function countSmileys that should return the total number of smiling faces.
Rules for a smiling face:
Each smiley face must contain a valid pair of eyes. Eyes can be marked as : or ;
A smiley face can have a nose but it does not have to. Valid characters for a nose are - or ~
Every smiling face must have a smiling mouth that should be marked with either ) or D
No additional characters are allowed except for those mentioned.
Valid smiley face examples: :) :D ;-D :~)
Invalid smiley faces: ;( :> :} :]
(Count the smiley faces!)
```html
//return the total number of smiling faces in the array
function countSmileys(arr) {
return arr.filter( face => /[:;]{1}[-~]?[)D]{1}/.test(face) ).length;
}
```
____
# Задание 10
Move the first letter of each word to the end of it, then add "ay" to the end of the word. Leave punctuation marks untouched.(Simple Pig Latin)
```html
function pigIt(str){
  //Code here
  const arr = str.split(' ')
  return arr
  .map((word) => {
   return word.match(/[A-z]/i)
   ? `${word.substr(1)}${word.substr(0, 1)}ay`
   : word
   })
   .join(' ')
}
```
