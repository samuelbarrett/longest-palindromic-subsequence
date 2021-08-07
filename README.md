# longest-palindromic-subsequence

This is my dynamic programming solution to a LeetCode problem (#516) which asks to reutrn the longest palindromic subsequence of a given String.
Longest palindromic subsequence is the longest sequence (consecutivity not required) of characters within the String that read identically forwards and backwards.

My solution uses Memoization (or, top-down dynamic programming) to build a solution by calculating required subproblems on-demand, recursively. This approach avoids costly and unnecessary re-computation of overlapping subproblems to return a result in O(n^2) time. A brute force solution would take about O(2^n) time to examine every possible subsequence.

I made this repository to keep the solution handy if I ever need a good example/reference of Memoization.
