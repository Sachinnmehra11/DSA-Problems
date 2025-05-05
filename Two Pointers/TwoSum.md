# 🧮 Problem 01: Two Sum

## 🔗 Problem Link
[LeetCode - Two Sum](https://leetcode.com/problems/two-sum/)

---

## 📌 Problem Statement

Given an array of integers `nums` and an integer `target`, return the indices of the two numbers such that they add up to the target.

- You may assume that each input would have **exactly one solution**.
- You may **not use the same element twice**.
- You can return the answer in **any order**.

---

## 🧪 Examples

### Example 1:

Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].
Example 
Input: nums = [3,2,4], target = 6
Output: [1,2]
Example 
Input: nums = [3,3], target = 6
Output: [0,1]


### Solution


---

## 🧠 Brute-Force Solution

```javascript
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
var twoSum = function(nums, target) {
    for (let index1 = 0; index1 < nums.length; index1++) {
        for (let index2 = index1 + 1; index2 < nums.length; index2++) {
            if (nums[index1] + nums[index2] === target) {
                return [index1, index2];
            }
        }
    }
};
