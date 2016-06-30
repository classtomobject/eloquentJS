# Chapter 2

###  Looping a Triangle

> Write a loop that makes seven calls to console.log to output the following triangle:

```
#
##
###
####
#####
######
#######
```

### Solution

```
var content = '';

for (var i = 0; i < 7; i ++){
  content = content + '#';
  console.log(content);
}
```

Description:
By creating an empty string, I am able to use a for loop that:
- initializes loop by creating the counter variable "i"
- setting an expression to check continuation of loop
- updates the loop by incrementing by 1 every iteration


### FizzBuzz

> Write a program that uses console.log to print all the numbers from 1 to 100, with two exceptions. For numbers divisible by 3, print "Fizz" instead of the number, and for numbers divisible by 5 (and not 3), print "Buzz" instead.
FizzBuzz for numbers divisible by both 3 & 5.

```
for (var i = 1; i <= 100; i++) {
  if ((i % 3 == 0) && (i % 5 == 0)) {   
    console.log('FizzBuzz')
  }
  else if (!(i % 3 == 0) && (i % 5 == 0)) {
    console.log('Buzz')
  }
  else if (i % 3 == 0) {
    console.log('Fizz')
  }
  else {
    console.log(i)
  }
}
```

Description:
Similar to previous example, I wanted to loop through the numbers 1-100.  <br />
At each number, I wanted to check:
<ul>
<li>number is divisible by 3</li>
<li>number is divisible by 5 and NOT 3</li>
<li>number is divisible by both 3 AND 5</li>
</ul>
Initially, I put the first condition in the if/else statement. However, that only gives me the error of not checking the third condition because as soon as it is satisfied, it begins to check the next number.
<br />
Thus, by putting the third condition first, this will work.
