# 🧮 Problem 02: Reverse String

## 🔗 Problem Link
[LeetCode - Two Sum](https://leetcode.com/problems/reverse-string/)


---

# 344. Reverse String

Write a function that reverses a string. The input string is given as an array of characters s.

You must do this by modifying the input array in-place with O(1) extra memory.

 

## 🧪 Examples

Input: s = ["h","e","l","l","o"]
Output: ["o","l","l","e","h"]
Example 2:

Input: s = ["H","a","n","n","a","h"]
Output: ["h","a","n","n","a","H"]

---

### Solution

## 🧠 Mirror Image Approach-

logic is we are setting a pointer at 0th position and itrating it to the end of half of s.length and then we are assigning s[i] with s[j-i] and s[j-i]=s[i] and 

```javascript

/**
 * @param {character[]} s
 * @return {void} Do not return anything, modify s in-place instead.
 */
var reverseString = function(s) {
    let j=s.length-1;
    for(let i=0; i < Math.floor(s.length/2);i++){
        [s[i],s[j-i]]=[s[j-i],s[i]]
    }
    
};

