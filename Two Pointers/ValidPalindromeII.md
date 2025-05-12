## Valid Palindrome II

## 🔗 Problem Link
[LeetCode - Valid Palindrome 2](https://leetcode.com/problems/valid-palindrome-ii/description/)

Given a string `s`, return `true` if the string can be a palindrome after deleting **at most one character** from it.

### Examples

**Example 1:**

Input: s = "aba"
Output: true


**Example 2:**

Input: s = "abca"
Output: true
Explanation: You could delete the character 'c'.


**Example 3:**

Input: s = "abc"
Output: false


### Solution (JavaScript)

```javascript
/**
 * @param {string} s
 * @return {boolean}
 */
var validPalindrome = function(s) {
    let start = 0;
    let end = s.length - 1;
    while (start < end) {
        if (s[start] !== s[end]) {
            return isPalindrome(s, start + 1, end) || isPalindrome(s, start, end - 1);
        } else {
            start++;
            end--;
        }
    }
    return true;
};

function isPalindrome(s, i, j) {
    let left = i;
    let right = j;
    while (left < right) {
        if (s[left] === s[right]) {
            left++;
            right--;
        } else {
            return false;
        }
    }
    return true;
}
