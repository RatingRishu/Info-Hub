## Array Methods

### `push()`: Add data to the end
let arr = ['Apple', 'Banana', 'Strawberry'];
arr.push('Mango');    // returns updated length i.e: 4
console.log(arr);     // ['Apple', 'Banana', 'Strawberry', 'Mango']

#pop() Remove data from the end

Eg:   let arr = ['Apple', 'Banana', 'Strawberry'];
	arr.pop();    // return a data which is popping out i.e: Strawberry
	console.log(arr);    // ['Apple', 'Banana']

#shift() Remove data from the start

Eg:   let arr = ['Apple', 'Banana', 'Strawberry'];
	arr.shift();    // return a data which is popping out i.e: Apple
	console.log(arr);    // ['Banana', 'Strawberry']

#unshift() Add data to the start

Eg:   let arr = ['Apple', 'Banana', 'Strawberry'];
	arr.unshift('Mango');    // return updated length i.e: 4
	console.log(arr);    // ['Mango', Apple', 'Banana', 'Strawberry']
	
#includes() Look for a value and returns true or false

Eg:    let arr = ['Apple', 'Banana', 'Strawberry'];
	arr.includes('Mango');    // returns false

Also have an optional argument from where to start searching.

#indexOf() Searches for a value and if it founds it, returns the index of it. And if it doesn't found returns -1.

Eg:    let arr = ['Apple', 'Banana', 'Strawberry'];
	arr.indexOf('Strawberry');    // returns 2
	
Also have an optional argument from where to start searching.

	• join() Creates a string from an array. Can add a separator in an argument by default ',' is a separator.
Eg:    let arr = ['a', 'b', 'c'];
	console.log(arr.join());    // "a,b,c"

	• reverse() Reverses an array in place (Actually changes an array).
Eg:    let arr1 = ['a', 'b', 'c', 'd'];
	console.log(arr1);    // ['a', 'b', 'c', 'd']
	arr1.reverse();
	console.log(arr1);    // ['d', 'c', 'b', 'a']
	
	• slice() Copy portion of an array from begin to end (end not included)
Eg:    let arr = ['CAT', 'DOG', 'TIGER', 'LION', 'ELEPHANT', 'GIRAFFE', 'FOX'];
	console.log(arr.slice(2));         // ['TIGER', 'LION', 'ELEPHANT', 'GIRAFFE', 'FOX']
	console.log(arr.slice(2, 6));    // ['TIGER', 'LION', 'ELEPHANT', 'GIRAFFE']
	console.log(arr.slice(2, 7));    // ['TIGER', 'LION', 'ELEPHANT', 'GIRAFFE', 'FOX']

	• splice() remove/replace element of an array.
Eg:    let arr = ['CAT', 'DOG', 'TIGER', 'LION', 'ELEPHANT', 'GIRAFFE', 'FOX'];
	arr.splice(2, 0, 'Bear');
	console.log(arr);    // ['CAT', 'DOG', 'Bear', 'TIGER', 'LION', 'ELEPHANT', 'GIRAFFE', 'FOX']

Array Callback functions
	• forEach() Accepts a callback function, and calls the function once per element in an array.

Eg: 
	const numsForEach = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
	numsForEach.forEach(function (n) {
	    console.log(n * 2);     // 2,4,6,8,10,12,14,16,18,20
	})

	• map() Creates a new array with the results of calling a callback on every element in the array.
Eg:
	const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
	const doubles = numbers.map(function (num) {
	    return num * 2;
	});
	console.log(doubles);   // [2, 4, 6, 8, 10, 12, 14, 16, 18, 20]

	• filter() Creates a new array with all the elements that passes the test implemented by the provided function.
Eg:
	numsFilter = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
	const evenNums = numsFilter.filter(num => num % 2 == 0);
	console.log(evenNums);      // [2, 4, 6, 8, 10]

	• find() Returns the value of the first element in the array that satisfies the provided testing function.
Eg:
	const movie = moviesFind.find(movie => {
	    return movie.includes('Mrs');
	});
	console.log(movie);     // "Mr. and Mrs. Smith"
	
	const movie2 = moviesFind.find(movie => movie.indexOf('Mrs') === 0);
	console.log(movie2);    // "Mrs. Doubtfire"

	• reduce() Executes a reducer function on each element of the array, resulting in a single value.
Eg: 
	const numsRed = [2, 3, 4, 5, 6];
	const product = numsRed.reduce((total, currentVal) => {
	    return total * currentVal;
	});
	console.log("Product: ", product);      // 720

	• some() Returns true if any of the array elements pass the test function.
Eg: 
	const words2 = ['dog', 'jello', 'log', 'cupcake', 'bag', 'wag'];
	// Are there any words longer than 4 letters
	const any4Lets = words2.some(word => {
	    return word.length > 4;
	});
	console.log(any4Lets);      // true

	• every() Returns a boolean value, tests whether all elements in the array passes the provided function.
Eg: 
	const words = ['dog', 'dig', 'log', 'bag', 'wag'];
	const all3Lets = words.every(w => {
	    return w[w.length - 1] === 'g';
	});
	console.log(all3Lets);  // true

	• sort() Sorts an array. By default it sorts like first convert every thing to string and then sorts. So for some cases behave differently.
Eg:
	const prices = [400.50, 3000, 99.99, 35.99, 12.00, 9500];
	console.log(prices.slice().sort());     // [12, 3000, 35.99, 400.5, 9500, 99.99]

But as we have studied callback function, now let's look into it again.

Eg:
	// Sorting in ascending order
	const ascSort = prices.slice().sort((a, b) => a - b);
	console.log("AscSort: ", ascSort);
	// Sorting in descending order
	const dscSort = prices.slice().sort((a, b) => b - a);
console.log("DscSort: ", dscSort);![image](https://github.com/RatingRishu/Info-Hub/assets/79776108/9e19c62d-7030-4495-b424-1112b63072a8)
