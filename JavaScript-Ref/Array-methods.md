## Array Methods

### `push():` Add data to the end
Eg: <br>
let arr = ['Apple', 'Banana', 'Strawberry']; <br>
arr.push('Mango');    // returns updated length i.e: 4 <br>
console.log(arr);     // ['Apple', 'Banana', 'Strawberry', 'Mango'] <br>

### `pop():` Remove data from the end

Eg: <br>
let arr = ['Apple', 'Banana', 'Strawberry']; <br>
arr.pop();    // return a data which is popping out i.e: Strawberry <br>
console.log(arr);    // ['Apple', 'Banana'] <br>

### `shift():` Remove data from the start

Eg: <br>
let arr = ['Apple', 'Banana', 'Strawberry']; <br>
arr.shift();    // return a data which is popping out i.e: Apple <br>
console.log(arr);    // ['Banana', 'Strawberry'] <br>

### `unshift():` Add data to the start

Eg: <br>
let arr = ['Apple', 'Banana', 'Strawberry']; <br>
arr.unshift('Mango');    // return updated length i.e: 4 <br>
console.log(arr);    // ['Mango', Apple', 'Banana', 'Strawberry'] <br>
	
### `includes():` Look for a value and returns true or false

Eg: <br>
let arr = ['Apple', 'Banana', 'Strawberry']; <br>
arr.includes('Mango');    // returns false <br>
<br>
This method also have an optional argument from where to start searching.

### `indexOf():` Searches for a value and if it founds it, returns the index of it. And if it doesn't found returns -1.

Eg: <br>
let arr = ['Apple', 'Banana', 'Strawberry']; <br>
arr.indexOf('Strawberry');    // returns 2 <br>
	
Also have an optional argument from where to start searching.

### `join():` Creates a string from an array. Can add a separator in an argument by default ',' is a separator.

Eg: <br>
let arr = ['a', 'b', 'c']; <br>
console.log(arr.join());    // "a,b,c" <br>

### `reverse():` Reverses an array in place (Actually changes an array).

Eg: <br>
let arr1 = ['a', 'b', 'c', 'd']; <br>
console.log(arr1);    // ['a', 'b', 'c', 'd'] <br>
arr1.reverse(); <br>
console.log(arr1);    // ['d', 'c', 'b', 'a'] <br>
	
### `slice():` Copy portion of an array from begin to end (end not included)

Eg: <br>
let arr = ['CAT', 'DOG', 'TIGER', 'LION', 'ELEPHANT', 'GIRAFFE', 'FOX']; <br>
console.log(arr.slice(2));         // ['TIGER', 'LION', 'ELEPHANT', 'GIRAFFE', 'FOX'] <br>
console.log(arr.slice(2, 6));    // ['TIGER', 'LION', 'ELEPHANT', 'GIRAFFE'] <br>
console.log(arr.slice(2, 7));    // ['TIGER', 'LION', 'ELEPHANT', 'GIRAFFE', 'FOX'] <br>

### `splice():` remove/replace element of an array.

Eg: <br>
let arr = ['CAT', 'DOG', 'TIGER', 'LION', 'ELEPHANT', 'GIRAFFE', 'FOX']; <br>
arr.splice(2, 0, 'Bear'); <br>
console.log(arr);    // ['CAT', 'DOG', 'Bear', 'TIGER', 'LION', 'ELEPHANT', 'GIRAFFE', 'FOX'] <br>

## Array Callback functions

### `forEach():` Accepts a callback function, and calls the function once per element in an array.

Eg: <br>
const numsForEach = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]; <br>
numsForEach.forEach(function (n) { <br>
	console.log(n * 2);     // 2,4,6,8,10,12,14,16,18,20 <br>
}) <br>

### `map():` Creates a new array with the results of calling a callback on every element in the array.

Eg: <br>
const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]; <br>
const doubles = numbers.map(function (num) { <br>
	return num * 2; <br>
}); <br>
console.log(doubles);   // [2, 4, 6, 8, 10, 12, 14, 16, 18, 20] <br>

### `filter():` Creates a new array with all the elements that passes the test implemented by the provided function.

Eg: <br>
numsFilter = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]; <br>
const evenNums = numsFilter.filter(num => num % 2 == 0); <br>
console.log(evenNums);      // [2, 4, 6, 8, 10] <br>

### `find():` Returns the value of the first element in the array that satisfies the provided testing function.

Eg: <br>
const movie = moviesFind.find(movie => { <br>
	return movie.includes('Mrs'); <br>
}); <br>
console.log(movie);     // "Mr. and Mrs. Smith" <br>
const movie2 = moviesFind.find(movie => movie.indexOf('Mrs') === 0);<br>
console.log(movie2);    // "Mrs. Doubtfire" <br>

### `reduce():` Executes a reducer function on each element of the array, resulting in a single value.

Eg: <br>
const numsRed = [2, 3, 4, 5, 6]; <br>
const product = numsRed.reduce((total, currentVal) => { <br>
	return total * currentVal; <br>
}); <br>
console.log("Product: ", product);      // 720 <br>

### `some():` Returns true if any of the array elements pass the test function.

Eg: <br>
const words2 = ['dog', 'jello', 'log', 'cupcake', 'bag', 'wag']; <br>
// Are there any words longer than 4 letters <br>
const any4Lets = words2.some(word => { <br>
	return word.length > 4; <br>
}); <br>
console.log(any4Lets);      // true <br>

### `every(): Returns a boolean value, tests whether all elements in the array passes the provided function.

Eg: <br>
const words = ['dog', 'dig', 'log', 'bag', 'wag']; <br>
const all3Lets = words.every(w => { <br>
	return w[w.length - 1] === 'g'; <br>
}); <br>
console.log(all3Lets);  // true <br>

### `sort():` Sorts an array. By default it sorts like first convert every thing to string and then sorts. So for some cases behave differently.

Eg: <br>
const prices = [400.50, 3000, 99.99, 35.99, 12.00, 9500]; <br>
console.log(prices.slice().sort());     // [12, 3000, 35.99, 400.5, 9500, 99.99] <br>
<br>
But as we have studied callback function, now let's look into it again.
<br>
Eg: <br>
// Sorting in ascending order <br>
const ascSort = prices.slice().sort((a, b) => a - b); <br>
console.log("AscSort: ", ascSort); <br>
// Sorting in descending order <br>
const dscSort = prices.slice().sort((a, b) => b - a); <br>
console.log("DscSort: ", dscSort); <br>
