# Minimize-the-LCS-Power

In a world of enchanted texts, Riya is given a magical task by a wise sage. She receives two strings, A and B, both of length N, filled with mystical lowercase English letters. Her quest is to minimize the power of their Longest Common Subsequence (LCS), which represents the shared magical bond between the two strings. However, Riya has the freedom to rearrange the letters in both strings in any way she wishes to weaken this bond.
Help Riya discover the minimum possible length of the LCS between the two strings, once she rearranges them optimally to break the shared power.

from collections import Counter  
  
def minimize_lcs_power(n, a, b):  

   count_a = Counter(a)  
   count_b = Counter(b)  
  
   common_counts = count_a & count_b  
  
   return max(common_counts.values(), default=0)  
  
t = int(input())  
  
for _ in range(t):  
   n = int(input())  
  
   a = input()  
   b = input()  
  
   print(minimize_lcs_power(n, a, b))
