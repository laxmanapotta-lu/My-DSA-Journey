Problem: LC-7-Reverse Integer
Link: https://leetcode.com/problems/reverse-integer/
Difficulty:Medium
Topic:Math
Pattern: Brute force by using while loop and reverse it

Understand the Question:
Here in the Question the question asks that can you reverse the given number without changing the postion of negative sign 

#Approach-1:
First we store the sign value and assign the negative sign at last after reversing the given number by using while 

#Code(Python):
class Solution:
    def reverse(self, x: int) -> int:
            sign=-1 if x<0 else 1
            x=abs(x)
            rev=0
            while(x!=0):
                digit=x%10
                rev=rev*10 + digit
                x=x//10

            if rev< -2**31 or rev> 2**31-1:
                return 0
            return rev*sign

Time Complexity:
O(logx)
This loop runs once for each digit in x.
If x has d digits , loop runs d times 
Space Complexity:
O(1)
Because, Here we didn't use any data type
What I Learned:
>Important thing is that main constain at end
>>>Here, rev<-2**31 or rev> 2**31-1
> Better approach

