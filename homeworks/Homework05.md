1. What is the difference between amortized analysis and average-case analysis? Why is ammortized analysis important?

2. In a stack, say we would like to perform a sequence of `n` PUSH, POP, and MULTIPOP operations, i.e. n operations total. Discuss how this sequence of `n` operations cost O(n<sup>2</sup>) using the average-case analysis but only O(n) using aggregate analysis.

3. In the context of aggregate analysis, for the `incrementing a binary counter` problem, derive and/or discuss the expression for `the total number of flips` when we perform a sequence of `n` INCREMENT operations. Assume that the number of bits is k. Why is this calculation important?

4. If the set of stack operations included a MULTIPUSH operation, which pushes `k` items onto the stack, would O(1) bound on the amortized cost of stack operations continue to hold? Discuss. (CLRS 17.1-1). 
