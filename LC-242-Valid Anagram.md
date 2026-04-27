Problem: LC-242-Valid Anagram
Link:https://leetcode.com/problems/valid-anagram/
Difficulty:Easy
Topic:Hashmap
Pattern: Just implemntation of hashmap

Understand the Question:
Here in the Question the question asks that given two strings check if both are anagram or not
Given two strings s and t, return true if t is an anagram of s, and false otherwise.

 #Approach-1:
 To solve this question we just create two hasmaps like freq={} and seen={} like this and count frequency of chars of first string and do once more for another string check it 

 #Code(Python):
 class Solution:
    def isAnagram(self, s: str, t: str) -> bool:
        freq={}
        seen={}
        for string in s:
            if string in freq:
                freq[string]+=1
            else:
                freq[string]=1


        for string in t:
            if string in seen:
                seen[string]+=1
            else:
                seen[string]=1


        if freq==seen:
            return True
        else:
            return False
                    
Time Complexity:
In worst Case:(means when both stings have no unique characters)
O(n+m)
n for first string and m for second string have different length
In best Case:
O(k)
when both strings have same size

Space Complexity:
In Worst Case:
O(n+m)
In best Case:
O(k)

What I learned:
>How to implement Hashmaps
>Brute Force approach