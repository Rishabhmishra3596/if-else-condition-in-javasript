function lucky_sevens(arr) {
  
  // if less than 3 elements then this challenge is not possible
  if (arr.length < 3) {
    return "not possible";
  }
  
  // because we know there are at least 3 elements we can
  // start the loop at the 3rd element in the array (i=2)
  // and check it along with the two previous elements (i-1) and (i-2)
  for (var i = 2; i < arr.length; i++) {
    if (arr[i] + arr[i-1] + arr[i-2] === 7) {
      return true; 
    }
  }
  
  // if loop is finished and no elements summed to 7
  return false;
  
}


 let array1 = [1, 2, 3, 4, 5]; // No triplet sums to 7
 let array2 = [2, 3, 2, 4, 1]; // Triplet [2, 3, 2] sums to 7

console.log(lucky_sevens(array1)); // Output: false
 console.log(lucky_sevens(array2)); // Output: true
