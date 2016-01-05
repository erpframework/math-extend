## Array native class extensions ##

**randomDraw**
```
randomDraw([n = 1]) -> Array
```
Does a random draw of n items from an array, and returns the result in a new array. Original array remains unchanged.

```
[1, 2, 3, 4, 5].randomDraw()   //->  [4]
[1, 2, 3, 4, 5].randomDraw(1)  //->  [5]
[1, 2, 3, 4, 5].randomDraw(2)  //->  [3, 2]
[1, 2, 3, 4, 5].randomDraw(4)  //->  [5, 1, 4, 3]
[1, 2, 3, 4, 5].randomDraw(5)  //->  [2, 4, 1, 3, 5]
```

---


**shuffle**
```
shuffle([inline = true]) -> Array
```
Returns a shuffled version of an array. By default, directly shuffles the original. If inline is set to false, uses a clone of the original array.

```
[1, 2, 3, 4, 5].shuffle()  //->  [4, 2, 1, 5, 3]
[1, 2, 3, 4, 5].shuffle()  //->  [1, 5, 3, 2, 4]
[1, 2, 3, 4, 5].shuffle()  //->  [5, 1, 4, 3, 2]
[1, 2, 3, 4, 5].shuffle()  //->  [2, 4, 1, 3, 5]
```

---


**swap**
```
swap(firstIndex, secondIndex) -> Array
```
Swaps 2 elements inside an array. Returns the modified array.

```
[1, 2].swap(0, 1)          //-> [2, 1]
[1, 2, 3, 4, 5].swap(0, 3) //-> [4, 2, 3, 1, 5]
```

---


[back to main wiki page](MathExtendDoc.md)