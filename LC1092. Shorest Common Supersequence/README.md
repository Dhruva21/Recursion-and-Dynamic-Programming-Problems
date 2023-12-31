# Problem Statement
Given two strings str1 and str2, return the shortest string that has both str1 and str2 as subsequences. If there are multiple valid strings, return any of them.

A string s is a subsequence of string t if deleting some number of characters from t (possibly 0) results in the string s.

Example 1:
Input: str1 = "abac", str2 = "cab"
Output: "cabac"
Explanation: 
str1 = "abac" is a subsequence of "cabac" because we can delete the first "c".
str2 = "cab" is a subsequence of "cabac" because we can delete the last "ac".
The answer provided is the shortest such string that satisfies these properties.
Example 2:

Input: str1 = "aaaaaaaa", str2 = "aaaaaaaa"
Output: "aaaaaaaa"

# Intuition
let s1, s2 be two strings of length n, m.
Ultimately the shortest common supersequence would be n + m + LCS(s1, s2). LCS --> Longest common subsequence
By solving the longest common subsequence problem using dp table, by traversing from the last block to above we can find the shortest common supersequence.
