This javascript extension for Prototype.js aims to provide more basic tools and functions for math-related development. It extends Math native object, Number and Array native classes.

Please visit the [Wiki section](MathExtendDoc.md) for some documentation.

The Prototype.js javascript framework can be found at http://www.prototypejs.org .



```


/*** Here are some examples of what you can do with math-extend. ***/



// Get the mean value of an array of numbers:

Math.mean([1, 2, 3, 4, 5]); // -> returns 3


// Get the standard deviation value of an array of numbers:

Math.stdDev([78, 88, 93, 67, 89, 75, 91]); // -> returns approximately 9


// Shuffle an array, which can contain elements of any kind:

['Hello', 'World', 1, 2, 3].shuffle(); // -> possible output: [3, 'World', 1, 'Hello', 2]

// Or, randomly select some items from an array:

[3, 7, 12, 21, 5, 1, 9].randomDraw(3); // -> returns a new array containing 3 selected items(in this example, could be [21, 9, 7])


// A bit of syntactic sugar with arrays:

var myArray = [1, 2, 3, 4, 5];
var len = myArray.shuffle().length; // now, value of len is 5, and myArray is shuffled


// tests on some numbers:

var myNumber = -12;
myNumber.isEven();     // -> returns true
myNumber.isOdd();      // -> returns false
(153303).isEven();     // -> returns false

myNumber.isInteger();  // -> returns true
myNumber.isNatural();  // -> returns false

(3).isPrime();         // -> returns true, 3 is a prime number
(4).isPrime();         // -> returns false, 4 is not a prime number


// a new way to calculate:

(12345).compute(function(myNumber) {
        // do a lot of custom stuff here!

        return anotherFunction(myNumber);
});

Number#compute can be chained:

(10).compute(function(n) {
    // custom stuff
    return n * 2;
}).compute(function(n) {
    // more custom stuff
    return n * 4;
});    // -> returns 80


// more stuff to come ..

```