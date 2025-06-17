# LeetCode Solutions

---

## Problem: [1768. Merge Strings Alternately](https://leetcode.com/problems/merge-strings-alternately/description/)

```javascript
/**
 * @param {string} word1
 * @param {string} word2
 * @return {string}
 */
var mergeAlternately = function(word1, word2) {
    let i=0;
    let j=0;
    let mergedString="";
    while(i<word1.length && j<word2.length){
        
        mergedString+=word1[i]+word2[j];
        i++;
        j++;
    }
    //using slice for remaining letters;
    if(i<word1.length){
        mergedString+=word1.slice(i);
    }
    if(i<word2.length){
        mergedString+=word2.slice(j);
    }
    return mergedString
};