# codewars-journal.md

### Challenge 1:

-**link:** https://www.codewars.com/kata/51f2d1cafc9c0f745c00037d/

- **description** Complete the solution so that it returns true if the first argument(string) passed in ends with the 2nd argument (also a string).
- **my solution** js
  function solution(str, ending) {
  return str.endsWith(ending);
  } -**what i learned** how to use the .endswith() method in js, it checks fi a string ends with specitic substring.

### challenge 2:

**link** https://www.codewars.com/kata/5899642f6e1b25935d000161/ -**description** You are given two sorted arrays that contain only integers. These arrays may be sorted in either ascending or descending order. Your task is to merge them into a single array, ensuring that:
The resulting array is sorted in ascending order.
Any duplicate values are removed, so each integer appears only once.
If both input arrays are empty, return an empty array.
No input validation is needed, as both arrays are guaranteed to contain zero or more integers. -**my solution** js
function mergeArrays(arr1, arr2) {
const combined = [...arr1, ...arr2];

const uniqueSet = new Set(combined);

return Array.from(uniqueSet).sort((a, b) => a - b);
}
console.log(mergeArrays([1, 2, 3, 4, 5], [6, 7, 8, 9, 10])); -**what i learned** used the spread operator (...) to merge two arrays,how to use a Set to remove duplicate values,You used Array.from() to turn a Set back into an array,sorted the array using a custom comparator

###  Challenge _3_:

- **Link:** [https://www.codewars.com/kata/562e98755e9214cd2500003d/]
- **Description:**  
   [Our friend Pac has finally decided to pursue a career in the coding industry.
  He is a newbie, he needs to learn properly.
  Therefore, Pac wants to apply for the worldwide famous -and very demanding-
  'C0d3r 1ns1d3' Academy for beginners.
  In order to join, Pac is required to solve a series of 3 exercises about 'Bug Fixes'.
  He has been sent an email from the Academy with the following instructions,
  Dear Pac,
  This is the first exercise. Find out what's wrong and fix the code.
  You have 15 minutes to send a solution.
  Good Luck.
  This code is a mess! Would you help Pac to fix the code in time?
  (This might be helpful -> Math.random();)
  This is my first Kata, so please any feedback (especially on Test Cases) is welcome!]

---

### My Solution

````js
function yourFutureCareer() {
  let career = Math.random();

  if (career <= 0.32) {
    return 'FrontEnd Developer';
  } else if (career <= 0.65) {
    return 'BackEnd Developer';
  } else {
    return 'Full-Stack Developer';
  }
}
console.log(yourFutureCareer());
-**what i learned**
Added a function name yourFutureCareer.

Replaced incorrect syntax (var :, return =, return :) with proper JavaScript:
let career = Math.random();
return 'Some Career';
Ensured strings like 'FrontEnd Developer' are wrapped in quotes.
Added proper curly braces and formatting for readability.

### Challenge 4:

- **Link:** [https://www.codewars.com/kata/5722b3f0bd5583cf44001000/]
- **Description:**
  [As you can see, the keys are the indices of the array elements. Important: When using for..in with an array, the key (index) is always a string, not a number. In the example above, the keys are "0", "1", and "2". We can't see the quotes because console.log() doesn't show them.

Although for..in can be used to traverse the array, this is discouraged because in some cases the order may be unexpected. So it's recommended that you use another variant for this: for..of (new in ES6). for..of can traverse all the values of the array (without accessing them through their index). Function showObjectValues() from above can be modified like this:

function showArrayValues(arr){]

---

###  My Solution
```js
function giveMeFive(obj) {
  let result = [];

  for (let key in obj) {
    if (key.length === 5) {
      result.push(key);
    }
    if (typeof obj[key] === "string" && obj[key].length === 5) {
      result.push(obj[key]);
    }
  }

  return result;
}
console.log(giveMeFive({apple: "juice", melon: "fruit", toast: "bread", hello: "world"}));

-**what i learned**
You learned how to use the for..in loop to iterate over the keys of an object, check the length of both keys and their values, and conditionally collect those with a length of 5 into an array.

###  Challenge _5_:

- **Link:** [https://www.codewars.com/kata/5822d89270ca28c85c0000f3/]
- **Description:**
  [Given a string and an array of indices, rearrange the characters of the string so that each character is placed at the position specified by the corresponding index in the array.]

---

###  My Solution
```js
function scramble(str, arr) {
  let result = [];
  for (let i = 0; i < arr.length; i++) {
    result[arr[i]] = str[i];
  }
  return result.join('');
}
scramble("abcd", [0, 3, 1, 2])
-**what i learned** how to reorder elements in a string based on an array of indices by mapping each character to its new position and then joining them back into a string.
````
