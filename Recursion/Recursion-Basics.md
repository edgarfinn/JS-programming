**Definition:**

The definition of a recursive function is a function that - at some point - calls itself.

**Three Key Ingredients to Recursion:**

  1. The Base Case (required)
  2. The Recursive Case (required)
  3. The Termination Case (optional)


```javascript
function countDown(num){
  if (num === 0) {
    return 1;
  }
  else {
    return countDown(num - 1)
  }
}
```

**1. The Base Case**

The base is a statement (normally an **if statement**) that determines when the recursion stops. In the above example:

```javascript
if (num === 0) {
  return 1;
}
```

**2. The Recursive Case**

This is where the function is called on itself.

**The recursive case must always lead the input towards the base case**

```javascript
return countDown(num-1)
```

Here the calling of ```countDown(num-1)``` ensures that the argument passed to the function will reduce by 1 each time, until eventually it reaches the base case, at which point the base case's code is executed to exit the recursion.

**3. The Termination Case**

This is a specific specific statement, which will stop the recursion in the event that the input is not capable of being lead to the base case. For example if you called ```countDown(-2)```, the function would not be able to count *down* to zero. Here's a variation of the countDown function, now including a **termination case**:

```javascript
function countDown(num){

  if (num < 0) {return console.log("enter a positive number")}

  else if (num === 0) {
    return 1;
  }
  else {
    console.log(num)
    return countDown(num - 1)
  }
}
countDown(-5)
// => enter a positive number
```

**External Links**

- [Recursion In Functional Javascript](https://www.sitepoint.com/recursion-functional-javascript/)
