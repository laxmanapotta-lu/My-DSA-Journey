Problem: LC-9-Palindrome Number
Link:https://leetcode.com/problems/palindrome-number/
Difficulty:Easy
Topic:Math
Pattern: String Slicing

Understand the Question:
Here in the question the question asks that when we read or check the given number on both sides or if the given number == when it reverse if both are same return True and if both are different return False

#Approach-1:
    convert the given number into string by using string method and then use string slicing convert the string in reverse order and check it out

#Code(Python)
class Solution:
    def isPalindrome(self, x: int) -> bool:
        y = str(x)[::-1]
        if str(x)==y:
            return True
        else:
            return False

Time Complexity:
O(n)
str(x) converts number to string → takes O(n)
[::-1] reverses string → takes O(n)
Comparing two strings → O(n)

So total:
O(n)

Space Complexity:
O(n)
Here we use new data type string 
So here memory used =O(n)

What I learned:
>How to implement String slicing method
>Better Approach because o(n)