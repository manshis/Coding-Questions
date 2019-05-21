
1. Find number of pairs in a given array whose difference is k.

```javascript
var arr = [1, 5, 3, 4, 2];
var k = 2;
let count = 0;
let left = 0;
let right = 0;
arr.sort();
while (right < arr.length) {
  let sum = arr[right] - arr[left];
  console.log(sum);
  if (sum == k) {
    count++;
    left++;
    right++;
  } else if (sum < k) {
    right++;
  } else if (sum > k) {
    left++;
  }
}
console.log(count);
```


