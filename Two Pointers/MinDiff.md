## Minimum Difference Between Highest and Lowest of K Scores

You are given a 0-indexed integer array `nums`, where `nums[i]` represents the score of the `iᵗʰ` student. You are also given an integer `k`.

Pick the scores of any `k` students from the array so that the difference between the highest and the lowest of the `k` scores is minimized.

Return the **minimum possible difference**.

### Examples

**Example 1:**

Input: nums = [90], k = 1
Output: 0
Explanation: There is one way to pick score(s) of one student:

[90]. The difference between the highest and lowest score is 90 - 90 = 0.
The minimum possible difference is 0.


**Example 2:**

Input: nums = [9,4,1,7], k = 2
Output: 2
Explanation: There are six ways to pick score(s) of two students:

[9,4], diff = 5

[9,1], diff = 8

[9,7], diff = 2

[4,1], diff = 3

[7,4], diff = 3

[7,1], diff = 6
The minimum possible difference is 2.


### Solution (JavaScript)

```javascript

/**
 * @param {number[]} nums
 * @param {number} k
 * @return {number}
 */
var minimumDifference = function(nums, k) {
    nums=nums.sort((a,b)=>a-b);  //js method to sort the array
    //nums=[1,4,7,9]
    let minDiff=Infinity;
    let left=0;
    let right=k-1;
    while(right<nums.length){
         let diff=nums[right]-nums[left]
        minDiff=Math.min(minDiff,diff);
        left++;
        right++;
    }
    return minDiff
};