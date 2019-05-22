2.  Find an element of the array such that the sum of all elements 
to the left is equal to the sum of all elements to the right.

```javascript
    var arr = [1, 2, 3, 3];
    var left = 0;
    var right = arr.length - 1;

    var leftSum = arr[left];
    var rightSum = arr[right];

    while (left != right) {
        if (leftSum < rightSum) {
            left++;
            leftSum += arr[left];
        }
        else {
            right--;
            rightSum += arr[right];
        }
    }

    if (leftSum == rightSum) {
        console.log('YES');
    } else {
        console.log('NO');
    }
    
```

