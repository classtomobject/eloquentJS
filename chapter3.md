# Chapter 3

### Minimum

> Write a function min that takes two arguments and returns their minimum.

### Solution

```
function min(x,y) {
  console.log(x < y ? x : y)
}
```

Description: <br />
Being new to JavaScript, I have never used the conditional (ternary) operator before. <br />
Using it here is quite useful. Given two variables, if x is less than y, then it will print x, if not, then y.
<br />

### Recursion

> We’ve seen that % (the remainder operator) can be used to test whether a number is even or odd by using % 2 to check whether it’s divisible by two. Here’s another way to define whether a positive whole number is even
or odd:
<ul>
<li>Zero is even.</li>
<li>One is odd.</li>
<li>For any other number N, its evenness is the same as N − 2.</li>
</ul>
Define a recursive function isEven corresponding to this description. The function should accept a number parameter and return a Boolean.
Test it on 50 and 75. See how it behaves on −1. Why? Can you think of a way to fix this?

<br />
```
function isEven(number) {
  if (number % 2 == 0) {
    console.log(true);
  }
  else if (number % 2 == 1) {
    console.log(false);
  }
  else {
    console.log(n > 0 ? isEven(n-2) : isEven(n+2));
  }
}
```

Description: <br />
Defining the function isEven, three conditions are given to satisfy what is needed.
<br />
<br />

### Bean Counting

>Write a function countBs that takes a string as its only argument and re- turns a number that 
indicates how many uppercase “B” characters are in the string.

<br />

```
function countBs(string) {
  var counter = 0;
  len = string.length;
  slice = string.split("");
  for (var i = 0; i < len; i++) {
    if (slice[i] == 'B') {
      counter++;
    }
  }
  console.log(counter);
}
```

Description: <br />
Decided to change things up and have a brute force approach. <br />
Function takes in a string and calculates the length, intialize a counter to count how many B's the string contains,
splits the string into separate characters, and then uses a for loop to iterate through and count up the amount of B's.
<br />
<br />
<br />

>Next, write a function called countChar that behaves like countBs, except it takes a second argument 
that indicates the character that is to be counted  (rather than counting only uppercase “B” characters). 
Rewrite countBs to make use of this new function.

```
function countLetters(string,letter) {
  var counter = 0;
  for (var i = 0; i < string.length; i++) {
    if (string.charAt(i) == letter) {
      counter++;
    }
  }
  console.log(counter);
}
```

Description: <br />
Similar to previous problem. Except now it allows specification of a letter.
