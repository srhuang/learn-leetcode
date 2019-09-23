---
description: '#Hash'
---

# \#001 Two Sum

## 題目

Given an array of integers, return **indices** of the two numbers such that they add up to a specific target.You may assume that each input would have _**exactly**_ one solution, and you may not use the _same_ element twice.

給定一個 array 和一個 target ，找出兩個數字加起來等於 target。

## 解法

### Naive

利用兩層迴圈直接找尋這兩個數字。

```c
int* twoSum(int* nums, int numsSize, int target) {
    int *solution=malloc(2 * sizeof(int));
    for(int i=0; i<numsSize-1; i++){
        for(int j=i+1; j<numsSize; j++){
            if((nums[i]+nums[j]) == target){
                solution[0]=i;
                solution[1]=j;
                break;
            }
        }
    }
    return solution;
}
```

#### Space Complexity

只有 solution 兩個數字的空間，所以是 $$O(1)$$。

#### Time Complexity

兩層迴圈總共花：\(n-1\) + \(n-2\) + \(n-3\) + ... + 1 = $$O(n^2)$$ 。

### Two-pass Hash Table





