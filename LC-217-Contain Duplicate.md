Problem: LC-217-Contains Duplicate
Link:https://leetcode.com/problems/contains-duplicate/
Difficulty:Easy
Topic:Arrays,Hashmap
Pattern:Just use to hasmaps and check it out

Understand the Question:
Here in the question the question asks that the given array contain duplicates or not if it contain duplicates return true otherwise false

#Approach-1:
Just create to hashmaps and count frequency of each element and increase count of the respective elemnt and finally check if both are equal return false otherwise True 
Here one important thing is that when implement of second hashmpap of set(nums)

#Code(Python):
class Solution:
    def containsDuplicate(self, nums: List[int]) -> bool:
        s=set(nums)
        freq={}
        seen={}

        for num in nums:
            if num in freq:
                freq[num]+=1
            else:
                freq[num]=1
        
        for num in s:
            if num in seen:
                seen[num]+=1
            else:
                seen[num]=1
        
        if freq==seen:
            return False
        else:
            return True

Time Complexity:
O(n)
Space complexity:
O(n)

What I learned:
> How to implement hashmaps and set operation here
>Best Approach
