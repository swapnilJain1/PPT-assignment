 **Q1.** Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

**Example:**
Input: nums = [2,7,11,15], target = 9
Output0 [0,1]

**Explanation:** Because nums[0] + nums[1] == 9, we return [0, 1]



```let arr = [7,1,5,3,6,4]

let target = 8

for(let i=0; i<arr.length;i++){
    for(let j=i+1;j<arr.length;j++){
        if(arr[i]+arr[j]===target){
            console.log(i,j)
        }
    }
}```

----------------------------------------------------------------------------------------------------------------------------------------------

💡 **Q2.** Given an integer array nums and an integer val, remove all occurrences of val in nums in-place. The order of the elements may be changed. Then return the number of elements in nums which are not equal to val.

Consider the number of elements in nums which are not equal to val be k, to get accepted, you need to do the following things:

- Change the array nums such that the first k elements of nums contain the elements which are not equal to val. The remaining elements of nums are not important as well as the size of nums.
- Return k.

**Example :**
Input: nums = [3,2,2,3], val = 3
Output: 2, nums = [2,2,_*,_*]

**Explanation:** Your function should return k = 2, with the first two elements of nums being 2. It does not matter what you leave beyond the returned k (hence they are underscores)


```let arr = [7,8,1,5,3,6,4,8,8,1]

let val = 8

let newArray = []

for(let i=0;i<arr.length;i++){
    if(arr[i]===val){
        continue
    }
    else{
        newArray.push(arr[i])
    }
}
console.log(newArray)```

---------------------------------------------------------------------------------------------------------------------------------------------

💡 **Q3.** Given a sorted array of distinct integers and a target value, return the index if the target is found. If not, return the index where it would be if it were inserted in order.

You must write an algorithm with O(log n) runtime complexity.

**Example 1:**
Input: nums = [1,3,5,6], target = 5

Output: 2

```let arr = [1,3,5,6,8,9]

let val = 7

for(let i=0;i<arr.length;i++){
    if(arr[i]===val){
        console.log(`number present at index : ${1}`)
        break
    }
    if(arr[i]>val){
        console.log(`Number would be added to index ${i}`)
            break
        }
    }```
    -----------------------------------------------------------------------------------------------------------------------------------------
  
💡 **Q6.** Given an integer array nums, return true if any value appears at least twice in the array, and return false if every element is distinct.

**Example 1:**
Input: nums = [1,2,3,1]

Output: true

```let arr = [1,3,5,5,6,8,9]
let count = 0

for(let i=0;i<arr.length;i++){
    for(let j=i+1;j<arr.length;j++){
        if(arr[i]===arr[j]){
            count++
        }
    }
}
let answer = count ? "True" : "False"
console.log(answer)```
--------------------------------------------------------------------------------------------------------------------------------------------

