## Number native class extensions ##

**compute**
```
compute(function) -> custom
```
Gets a custom function, having Number as its only parameter, and returns its result.

```
(123).compute(function(nb) {
        // do any custom stuff here ...
        return nb * 2;
})    //-> 246

(289341211).compute(function(nb) {
        return nb.isPrime();
});   //-> true

// hint for advanced Prototype users: the 'this' reference is available for an utility like Function#bind:

(100).compute(function(nb) {
        return nb + this.value;
}.bind({value: 10}));   //-> 110

```

---


**isEven**
```
isEven() -> Boolean
```
Returns true if Number is even, false otherwise.

```
(0).isEven()    //-> true
(1).isEven()    //-> false
(2).isEven()    //-> true
(4.38).isEven() //-> false
```

---


**isInteger**
```
isInteger([ excludeZero = false ]) -> Boolean
```
Returns true if Number is an integer, false otherwise.
If optional parameter excludeZero is set to true, test with number zero(0) will return false.

```
(0).isInteger()         //-> true
(0).isInteger(true)     //-> false
(-32).isInteger()       //-> true
Number('3').isInteger() //-> true
(2.45).isInteger()      //-> false
```

---


**isNaN**
```
isNaN() -> Boolean
```
Returns true if Number is 'not a number' (NaN), false otherwise. An instance-method version of native [isNaN()](http://www.w3schools.com/jsref/jsref_isNaN.asp).

```
(435632).isNaN()        //-> false
(0).isNaN()             //-> false
Number('34').isNaN()    //-> false
Number('Hello').isNaN() //-> true
```

---


**isNatural**
```
isNatural([ excludeZero = false ]) -> Boolean
```
Returns true if Number is an integer greater than or equal to zero(0), false otherwise.
If optional parameter excludeZero is set to true, test with number zero(0) will return false.

```
(0).isNatural()         //-> true
(0).isNatural(true)     //-> false
(-32).isNatural()       //-> false
Number('3').isNatural() //-> true
(2.45).isNatural()      //-> false
```

---


**isNull**
```
isNull() -> Boolean
```
Returns true if Number is equal to zero(0), false otherwise.

```
(4).isNull()             //-> false
(-6.35).isNull()         //-> false
(0).isNull()             //-> true
Number().isNull()        //-> true
Number('Hello').isNull() //-> false
```

---


**isOdd**
```
isOdd() -> Boolean
```
Returns true if Number is odd, false otherwise.

```
(0).isOdd()    //-> false
(1).isOdd()    //-> true
(2).isOdd()    //-> false
(4.38).isOdd() //-> false
```

---


**isPrime**
```
isPrime() -> Boolean
```
Returns true if Number is a prime, false otherwise. If tested number is greater than 1e+16, test will always return false because of javascript limitations(tested on Firefox 3.x).

```
(2).isPrime()         //-> true
(3).isPrime()         //-> true
(4).isPrime()         //-> false
(289341211).isPrime() //-> true
```

---


[back to main wiki page](MathExtendDoc.md)