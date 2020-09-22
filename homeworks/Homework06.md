# Homework 6

## Read sections 17.1 from CLRS
Please read this with the goal of using the knowledge to do the homework below.

## Watch the recorded lectures
1. [Huffman coding and Huffman trees](https://youtu.be/JsTptu56GM8)
1. [Tracing the Huffman's algorithm - How does the Huffman's algorithm work?](https://youtu.be/qE4tfsiTGjE)

## Question 1
What is the difference between amortized analysis and average-case analysis? Why is ammortized analysis important?

## Question 2
In an empty stack, say we would like to perform a sequence of `n` PUSH, POP, and MULTIPOP operations, i.e. n operations total. Discuss how this sequence of `n` operations cost O(n<sup>2</sup>) using the average-case analysis but only O(n) using aggregate analysis.

## Question 3
Say we would like to perform a sequence of `n` PUSH, POP, and MULTIPOP operations (i.e. n operations total) in a non-empty stack. Does the O(n) using aggregate analysis still hold true? Discuss.

## Question 4
In the context of aggregate analysis, for the `incrementing a binary counter` problem, derive and/or discuss the expression for `the total number of flips` when we perform a sequence of `n` INCREMENT operations. Assume that the number of bits is k. Why is this calculation important?

## Question 5
If the set of stack operations included a MULTIPUSH operation, which pushes `k` items onto the stack, would O(1) bound on the amortized cost of stack operations continue to hold? Discuss. (CLRS 17.1-1). 
