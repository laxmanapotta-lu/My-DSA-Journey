Problem: LC-1-Two Sum
Link: https://leetcode.com/problems/two-sum/
Difficulty: Easy
Topic:Arrays
Pattern: Brute Force by using Nested loops

Understand the Question:
Here in the question the question asks that when add two items from the given array 
If we get result as target return the indices of the two items(numbers)

#Approach-1:
Here first we use one for loop and access one element and once more we use another for loopto iterate through each element and check for each iteration is sum is equal to the target and runs upto the condition satisfied then return the indicies of the target satisfy elements

#Code(Python)
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        for i in range(len(nums)):
            for j in range(1+i ,len(nums)):
                if nums[i]+nums[j]==target:
                    return [i,j]

Time Complexity:
O(n**2)
Because of each element and using nested loops

Space Complexity:
O(1)
Because of no extra data structure used

What I Learned:
> How nested Loops work
> How to avoid checking same pair twice using j=i+1
> Brute force approach