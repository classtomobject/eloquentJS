<h1>Chapter 4</h1>

<h3>Sum of Range</h3>

>Write a range function that takes two arguments, start and end, and returns an array containing all the numbers from 
start up to (and including) end. <br><br>
Next, write a sum function that takes an array of numbers and returns the sum of these numbers.<br><br>
As a bonus assignment, modify your range function to take an optional third argument that indicates 
the “step” value used to build up the array.

<br>
<h3>Solution</h3>

```
function range(start,end) {
  var a = [start], b = start;
  while (b < end) {
    b++;
    a.push(b);
  }
  console.log(a);
}


var sum = array.reduce((prev,curr) => prev + curr, 0);
console.log(sum)


function range2(start, end, step){
  var a=[start], b=start;
  while(b < end-1){
    b+=step;
    a.push(b);
  }
  console.log(a);
};

```
Description: <br>
The first function range takes an initial and end number. Then produces an array of numbers incremented by 1. <br>
The second is a simple variable that uses the reduce method: reducing array to single value. <br>
The last is a variation of the first method, which adds a step size. <br>

<br>
<h3>Reversing An Array</h3>

>The first, reverseArray, takes an array as an argument and produces a new array that has the same elements 
in the inverse order. The second, reverseArrayInPlace, does what the reverse method does: it modifies the 
array given as argument in order to reverse its elements. <b>Neither may use the standard reverse method.</b>

```

function reverseArray(array) {
  newarray = []
  for (var i = array.length - 1; i >= 0; i--) {
    newarray.push(array[i]);
  }
  console.log(newarray)
}



function reverseArrayInPlace(array)
{
    for (var first = 0; first < array.length / 2; first += 1)
    {
        var second = array.length - first - 1;
        var swap = array[first];
        array[first] = array[second];
        array[second] = swap;
    }
    console.log(array);
}
```

Description:<br>
The first function starts by creating an empty array. Then by using a for loop, iterates through and adds contents of
attribute array to beginning of new array with the .push() method. <br>
The second function is similar but does not create or use an empty list. This one uses the swap method, with has 
known to be more efficient.
