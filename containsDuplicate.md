# Contains Duplicate

> [!NOTE]
> [LeetCode Link](https://leetcode.com/problems/contains-duplicate/description/)
> 
> Given an integer array nums, return true if any value appears at least twice in the array, and return false if every element is distinct.
> 
> __Example 1__: Input: nums = `[1,2,3,1]`, Output: `true`
> 
> __Example 2__: Input: nums = `[1,2,3,4]`, Output: `false`
> 
> __Example 3__: Input: nums = `[1,1,1,3,3,4,3,2,4,2]`, Output: `true`

## Solution 1

By utilizing a [`set`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set) we can immediately gain access to all unique elements inside of an array in O(1): 

> _`Set` objects are collections of values. A value in the set may only occur once._

Because `set` returns an object we can use [`.size`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set/size) to determine how many entries the set object has. If the numerical output of `.length` and `.size` do not match, we return true; else false

```TypeScript
function containsDuplicate(nums: number[]): boolean {  
    return new Set([...nums]).size !== nums.length
};
```

