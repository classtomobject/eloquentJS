# Chapter 2

###  Looping a Triangle

Write a loop that makes seven calls to console.log to output the following triangle:

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
