Question 2.1
// make a loop that goes from 1 to 100
for ( var num = 1; num < 101; num ++ ) {
  
  // check if the number is divisible by 3 or 5
  var checkForThree = num % 3;
  var checkForFive = num % 5;
  
  // if the number is divisible by both 3 and 5, then print FizzBuzz
  if ( (checkForThree == 0) && (checkForFive == 0) ) 
  	console.log( "FizzBuzz");
  
  // if the number is divisible by 3, then print Fizz
  else if (checkForThree == 0)
    console.log( "Fizz");
  
  // if the number is divisible by 5, then print Buzz
  else if (checkForFive == 0)
    console.log( "Buzz");
  
  // otherwise just print the number
  else
    console.log( num );
} 


Question 2.2 
var size = 8
var board = ""

for (var y = 0; y<size; y++){
  for (var x = 0; x<size; x++){
    if((x + y) % 2===0){board += " "}
    else{board += "#"}
  }
  board += "\n"
}

console.log(board)

Question 2.3
function range(start, end, step){
  var arr = [];
  var s = start;
  var e = end;
  step = step || 1;
  
  var comparator = function(incr, end){
    if(step < 0){
      return incr >= end;
    }
    else{
      return incr <= end;
    }
  };
  
  for(var i = s; comparator(i, e); i = i + step){
    arr.push(i);
  }
  
  return arr;
}

//Input: 2 integers.
//Output: Array of all integers within that range.
var range = function(arg1, arg2) {
  var arr = [];
  if (arg2 > arg1)
    for (var i = arg1; i <= arg2; i++)
      arr.push(i);
  else
    for (var j = arg1; j >= arg2; j--)
      arr.push(j);
  return arr;
}

//Input: 2 integers, 1 step value.
//Output: Array of all integers within that range, with the given step.
var range2 = function(arg1, arg2, step) {
  var arr = [];
  if (arg2 > arg1)
    for (var i = arg1; i <= arg2; i = i + step)
      arr.push(i);
  else
    for (var j = arg1; j >= arg2; j = j + step)
      arr.push(j);
  return arr;
}

//Input: An array.
//Output: The sum of all array values.
var sum = function(arr) {
  var sumVar = 0;
  for (var i = 0; i < arr.length; i++) 
    sumVar = sumVar + arr[i];
  return sumVar;
}

console.log(sum(range(1, 10)) + "\n");
// → 55

var array = range2(5, 2, -1);
for (var i = 0; i < array.length; i++) {
  console.log(array[i]);
} 

// → [5, 4, 3, 2]
