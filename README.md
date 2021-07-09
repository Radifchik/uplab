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
Write a function that will return the count of distinct case-insensitive alphabetic characters and numeric digits that occur more than once in the input string. The input string can be assumed to contain only alphabets (both uppercase and lowercase) and numeric digits.
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
Your task is to make a function that can take any non-negative integer as an argument and return it with its digits in descending order. Essentially, rearrange the digits to create the highest possible number.
```html
function descendingOrder(n){
  return parseInt(String(n).split('').sort().reverse().join(''))
}
```
____
# Задание 7
Given the triangle of consecutive odd numbers:
```html
             1
          3     5
       7     9    11
   13    15    17    19
21    23    25    27    29
...
```
Calculate the sum of the numbers in the nth row of this triangle (starting at index 1)
```html
function rowSumOddNumbers(n) {
	return Math.pow(n, 3);
}
```
____
# Задание 8
In this kata you will create a function that takes a list of non-negative integers and strings and returns a new list with the strings filtered out.
```html
function filter_list(l) {
  return l.filter(Number.isInteger);
}
```
____
# Задание 9
Given two integers a and b, which can be positive or negative, find the sum of all the integers between and including them and return it. If the two numbers are equal return a or b.
```html
function getSum( a,b )
{
  var min = Math.min(a, b),
  max = Math.max(a, b),
  result = 0;
  while (min <= max) {
    result += min;
    min++;
  }
  return result;
}
```
____
# Задание 10
You are given an odd-length array of integers, in which all of them are the same, except for one single number.

Complete the method which accepts such an array, and returns that single different number.
```html
function stray(numbers) {
    var a = numbers.sort();
  
  if(a[0] != a[1]) {
    return a[0]
  } 
  return a[a.length-1]
}
```
