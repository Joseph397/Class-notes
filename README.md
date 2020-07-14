# Class-notes
JavaScript 101

console.log('hello'); //                            9:00 minutes

// alert('hello this is Joseph');

// How to write a comment inline

// Variables
let b = 'smoothie';
console.log(b);

/*let someNumber = 45;
console.log(someNumber);
*/
/* Manipulate Dom with Javascript
...It's just a Fancy way of saying change HTML with Javascript
*/

//let age = prompt('What is your age?');

//document.getElementById('someText').innerHTML = age;

// Numbers in Javascript

/* let num1 = 5.7;   //Simple operations
console.log(5 * 10); // 50
console.log(50 / 5); // 10
8
*/

let num1 = 10;
// num = num1 + 1; Or

// Increment num1 by 1
num1++;
console.log(num1); // 11

// Decrement num1 by 1
num1--;
console.log(num1); // 9?

//Divide, multiply *, remainder %
console.log(num1 / 6); // 1.6666666666666667

// Increment/decrement by 10
num1 += 10;
console.log(num1); // 20

/*Functions
1.Create a function
2. Call the function
*/

//Create
function fun() {
    console.log('this is a function');
}
 
//Call                                                    24:33
fun(); // this is a function

/* Let's create a function that takes in a name and says hello followed by your name

For example

Name: "Joseph"
return: "Hello Joseph"
*/




function greeting(yourName) {
    let result = 'Hello ' + yourName; // String Concatenation
    console.log(result);
}

/*let name = prompt('What is your name?');
greeting(name); // Hello + Name input ^
*/

// How do arguments work in functions?
// How do we add 2 numbers together in a function?

function sumNumbers(num1, num2){
    let result = num1 + num2;
    console.log(result);
}

sumNumbers(10, 10); // 20 ^ 

//sumNumbers('Joseph ', 'Granville'); // Joseph Granville 

/* While loops                                            36:00

let num = 0;

while (num < 100) {
    num += 1;
    console.log(num);
}
*/

// For loop same as above but more efficient
for (let num = 0; num < 100; num++) {
    console.log(num);
}

// Data types
let yourAge = 18;                               // number
let yourName = 'Bob';                            // string
let name = {first: 'Jane', last: 'Doe'};        // object
let truth = false;                              // boolean
let groceries = ['apple', 'banana', 'oranges']; // array
let random;                                     // undefined
let nothing = null;                             // value null

//Strings in Javascript (common methods)
let fruit = 'banana,apple,orange,blackberry';
let moreFruits = 'banana\napple'; 
// console.log(moreFruits);// outputs 'banana' a line break and 'apple'

console.log(fruit.length); // 6 (number of characters)
// console.log(fruit.indexOf('an')); // 1 ( an is found first a index 1)
//console.log(fruit.indexOf('q')); // -1 not found
console.log(fruit.indexOf('nan')); // 2 (Returns the position of the first occurrence of a substring.)
console.log(fruit.slice(2, 4)); // na (slices from index 2 until index 4 of fruit)
console.log(fruit.slice(2, 6)); // nana (slices from index 2 until index 6)
console.log(fruit.slice(2, 5)); // nan (slices from index 2 until index 5)
console.log(fruit.replace('ban', '123')); // 123ana (replaces part of a string)
console.log(fruit.toUpperCase()); // BANANA
console.log(fruit.toLowerCase()); // banana
console.log(fruit.charAt(2)); // n (returns character at index 2)
console.log(fruit.split(',')); // (4) ["banana", "apple", "orange", "blackberry"] (Split a string into substrings using the specified separator(,) and return them as an array.
console.log(fruit.split('')); // (30) ["b", "a", "n", "a", "n", "a", ",", "a", "p", "p", "l", "e", ",", "o", "r", "a", "n", "g", "e", ",", "b", "l", "a", "c", "k", "b", "e", "r", "r", "y"] (split by character)

// Array                                                  52:00

let fruits = ['banana', 'apple', 'orange', 'pineapples'];
fruits = new Array('banana', 'apple', 'orange', 'pineapples');

// alert(fruits[1]); // (alerts fruit index 1)
console.log(fruits[2]); // orange (avcess value at index 2)

fruits[0] = 'pear'; // replaces first string fruits with pair
console.log(fruits);

for (let i = 0; i < fruits.length; i++) {
    console.log(fruits[i]); // returns the fruits individually
}

// array common methods                                 1:03:47
console.log('to string', fruits.toString());
console.log(fruits.join(' * ')); // pear * apple * orange * pineapples (Adds all the elements of an array separated by the specified separator string.)
console.log(fruits.pop(), fruits); // (3) ["pear", "apple", "orange"] (Removes the last element from an array and returns it.)
console.log(fruits.push('blackberries'), fruits); // 4) ["pear", "apple", "orange", "blackberries"] (Appends new elements to an array, and returns the new length of the array.)
console.log(fruits[4]);
fruits[fruits.length] = 'new fruit'; // (5) ["pear", "apple", "orange", "blackberries", "new fruit"] (same as push)
console.log(fruits);
fruits.shift(); // (4) ["apple", "orange", "blackberries", "new fruit"] (remove first element from an array)
console.log(fruits);
fruits.unshift('kiwi'); // (5) ["kiwi", "apple", "orange", "blackberries", "new fruit"] (add first element from an array)
console.log(fruits)

let vegetables = ['asparagus', 'tomato', 'broccoli'];
let allGroceries = fruits.concat(vegetables); // combine arrays
console.log(allGroceries); // (8) ["kiwi", "apple", "orange", "blackberries", "new fruit", "asparagus", "tomato", "broccoli"]
console.log(allGroceries.slice(1, 4));// (3) ["apple", "orange", "blackberries"] (Returns a section of an array.)
console.log(allGroceries.reverse());// (5) ["pear", "apple", "orange", "blackberries", "new fruit"](5) ["pear", "apple", "orange", "blackberries", "new fruit"] (Reverses the elements in an Array.)
console.log(allGroceries.sort()); // places in alphabetical order

let someNumbers = [5, 10, 2, 25, 3, 255, 1, 2, 5, 334, 321, 2];
// console.log(someNumbers.sort()); // orders numbers by numeric value ((12) [1, 10, 2, 2, 2, 25, 255, 3, 321, 334, 5, 5])
console.log(someNumbers.sort(function(a, b) {return a-b})); // (12) [1, 2, 2, 2, 3, 5, 5, 10, 25, 255, 321, 334] (sorted in ascending order)
console.log(someNumbers.sort(function(a, b) {return b-a})); // (12) [334, 321, 255, 25, 10, 5, 5, 3, 2, 2, 2, 1] (sorted in decending order)

let emptyArray = new Array();
for (let num = 0; num <= 10; num++) {
    emptyArray.push(num);
}
console.log(emptyArray);                              //1:11:00

//Objects in Javascript
// dictionaries in Python

let student = {
    first: 'Joseph',
    last: 'Granville',
    age:25,
    height:170,
    studentInfo: function () {
        return this.first + '\n' + this.last +'\n' +this.age;
    }
};

//console.log(student.first); // Joseph
//console.log(student.last); // Granville
//student.first = 'notJoseph'; // change value
// console.log(student.first); // notJoseph
student.age++; // 24 (incriment by 1)
console.log(student.age);

console.log(student.studentInfo()); //Joseph line break Granville line break 24

// Conditionals, Control flows (if else)                1:19:00
// 18-35 is my target demographic
// && abd
// || or
//let age = prompt('what is your age'); // whats your name prompt eith input
let age =  45;

if ((age >= 18) && (age <= 35) ) {
    status = 'target demo';
    console.log(status);
} else {
    status = 'not my audience';
    console.log(status);
}

// Switch statements
// differentiate between weekday vs. weekend
// day 0 --> Sunday --> weekend
// day 1 --> Monday --> weekday
// day 2 --> Tuesday --> weekday
// day 3 --> Wednesday --> weekday
// day 4 --> Thursday --> weekday
// day 5 --> Friday --> weekend
// day 6 --> Saturday --> weekend

switch (6) {
    case 0:
        text = 'weekend';
        break;
    case 5:
        text = 'weekend'
        break;
    case 6:
        text = 'weekend'
        break;
    default:
        text = 'weekday'
}
   
 console.log(text);                                 // 1:31:00


