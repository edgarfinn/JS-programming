** Basic Recursion **

### Count Down
```JavaScript
function countDown(num){
  //optional termination case
  if (num < 0) {return console.log("enter a positive number")}

  //base case
  else if (num === 0) {
    return 1;
  }
  //recursive case
  else {
    console.log(num)
    return countDown(num - 1)
  }
}
countDown(5)
/*

5 4 3 2 1
=> 1

*/
```

### Addition

Very basic addition function for positive integers.

```javascript
function add(num, toNum){
  if (toNum === 0) {
    return num;
  }
  else {
    return add(num+1, toNum-1)
  }
}

add(4,3)
// => 7
```

### Iterating through an string, and converting to an array

This requires a parent function, containing a nested recursive function. Its fairly pointless, given the ```.split("")``` method could be used for this. But illustrates the process of iterating through a given input with recursion.

```javascript


function convert(str){
  var arr = str.split(""), opArray = [];

  function recusiveIterate(i){
    if (i === arr.length) {
      return arr.length-1;
    }
    opArray.push(arr[i]);
    return recusiveIterate(i+1)
  }

  recusiveIterate(0);

  return opArray;

}

convert('abce')
=> [ 'a', 'b', 'c', 'e' ]

```
