---
title: 2020-01-17-ImplementStr
date: 2020-01-17 18:25:30
tags:
- Easy
categories:
- LeetCode
---
# LeetCode28
Implement strStr().

Return the index of the first occurrence of needle in haystack, or -1 if needle is not part of haystack.

Example 1:

Input: haystack = "hello", needle = "ll"
Output: 2
Example 2:

Input: haystack = "aaaaa", needle = "bba"
Output: -1
Clarification:

What should we return when needle is an empty string? This is a great question to ask during an interview.

For the purpose of this problem, we will return 0 when needle is an empty string. This is consistent to C's strstr() and Java's indexOf().

# Solution
如果不考虑java偷懒的写法当然可以想到indexof的想法
```java
class Solution {
    public int strStr(String haystack, String needle) {
        return haystack.indexOf(needle);
    }
}
Runtime: 1 ms
```
先按照题意写了如下代码：
```java
class Solution {
 public int strStr(String haystack, String needle) {
        if(needle.length()==0)return 0;
        if(haystack.length()==0)return -1;
        int index =-1;
        boolean flag = true;
        for(int i=0;i<haystack.length();i++){
            if(haystack.charAt(i)==needle.charAt(0)){
                flag=true;
                for(int j =0;j<needle.length();j++){
                    if(i+j>=haystack.length()){
                        return -1;
                    }
                    if(haystack.charAt(i+j)!=needle.charAt(j)){
                        flag=false;
                        break;
                    };
                }
                if(flag){
                    return  i;
                }
            }

        }
        return  index;
    }
}
Runtime: 4 ms
Memory Usage: 42.7 MB
```