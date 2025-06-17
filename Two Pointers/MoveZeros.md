# LeetCode Solutions

---

## Problem: [283. Move Zeroes](https://leetcode.com/problems/move-zeroes/description/)

##
Given an integer array nums, move all 0's to the end of it while maintaining the relative order of the non-zero elements.

Note that you must do this in-place without making a copy of the array.

 

Example 1:

Input: nums = [0,1,0,3,12]
Output: [1,3,12,0,0]
Example 2:

Input: nums = [0]
Output: [0]
 

Constraints:

1 <= nums.length <= 104
-231 <= nums[i] <= 231 - 1


## Solution
```javascript

/**
 * @param {number[]} nums
 * @return {void} Do not return anything, modify nums in-place instead.
 */
var moveZeroes = function (nums) {
    //using extra space
    // let arr=[];
    // for (let i=0;i<nums.length;i++){
    //     if(nums[i]!==0){
    //         arr.push(nums[i])
    //     }
    // }
    // while(arr.length!==nums.length){
    //     arr.push(0)
    // }
    // console.log(arr)
    // return arr

    let i = 0;
    let itr = 0;
    while (i < nums.length) {
        if (nums[i] === 0) {
            i++;
        } else {
            nums[itr] = nums[i];
            i++;
            itr++;
        }

    }
    console.log(itr)
    while (itr < nums.length) {
        nums[itr] = 0;
        itr++
    }
    return nums



};