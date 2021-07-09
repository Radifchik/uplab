# uplab

Задание 1
This code does not execute properly. Try to figure out why.(Multiply)

Код
function rowSumOddNumbers(n) {
  return n*n*n
}

Задание 2
Given the triangle of consecutive odd numbers(Sum of odd numbers)

Код
function rowSumOddNumbers(n) {
  return n*n*n
}

Задание 3 
Given an array of integers, find the one that appears an odd number of times.
There will always be only one integer that appears an odd number of times.

Код
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
