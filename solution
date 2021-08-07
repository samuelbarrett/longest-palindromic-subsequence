class Solution {
    public int longestPalindromeSubseq(String s) {
        int n = s.length();
        int[][] subProbSols = new int[n][n];
        // initialize all table entries to some unsolved value
        for(int i=0; i<s.length(); i++) {
            for(int j=0; j<s.length(); j++) {
                subProbSols[i][j] = -1;
            }
        }
        return palindromicSubseq(s, subProbSols, 0, n-1);
    }
    // using Dynamic Programming: Memoization/top-down technique for on-demand solving of
    // subproblems. Recursively solves the original problem by determining subproblem
    // calculations required to build solution.
    private int palindromicSubseq(String s, int[][] subProbSols, int i, int j) {
        if(subProbSols[i][j] == -1) {
            // base case - subsequence of size 1
            if(i == j) {
                subProbSols[i][j] = 1;
            }
            else if(s.charAt(i) == s.charAt(j)) {
                // sub sequence of size 2
                if(j == i+1) {
                    subProbSols[i][j] = 2;
                }
                // append s[i] and s[j] to the ends of the largest palindrome found between them.
                else {
                    subProbSols[i][j] = palindromicSubseq(s, subProbSols, i+1, j-1) + 2;
                }
            }
            // no palindrome includes both s[i] != s[j], find the largest subsequence from s[i+1..j] and s[i..j-1]
            else {
                subProbSols[i][j] = Math.max(
                    palindromicSubseq(s, subProbSols, i+1, j),
                    palindromicSubseq(s, subProbSols, i, j-1)
                );
            }
        }
        return subProbSols[i][j];
    }
}
