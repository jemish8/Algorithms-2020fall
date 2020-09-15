# Homework 4

## Read sections 16.1, 16.2, and 16.3 from CLRS
Please read this with the goal of using the knowledge to do the homework below.

## Watch the recorded lectures
- [Why study greedy algorithms?](https://youtu.be/gHWxmb_nVpY)
- [The activity selection problem for understanding greedy algorithms](https://youtu.be/tEfVXgrP6WU)
- [Optimal substructure of the activity selection problem](https://youtu.be/LmlHHSr7gys)
- [Intuition for understanding how greedy algorithms work](https://youtu.be/BWlXudP7Unk)
- [Recursive greedy algorithm for the activity selection problem](https://youtu.be/alybycFq2mU)


## Question 1
Explain the 'activity selection problem' by creating a problem of your own. You are free to create any problem, as long as it is similar to a standard activity selection problem.

## Question 2 (programming)
In Python, implement (a) a recursive solution, (b) a dynamic programming solution, (c) a recursive greey solution, and (d) an iterative greedy solution to the following activity selection problem.

i  |  1 |  2 |  3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11
-- | -- | -- | -- | -- | -- | -- | -- | -- | -- | --  | --
s<sub>i</sub> |  1 |  3 |  0 | 5 | 3 | 5 | 6 | 8 | 8 | 2 | 12 
f<sub>i</sub> |  4 |  5 |  6 | 7 | 9 | 9 | 10 | 11 | 12 | 14 | 16

## Question 3 (programming)
The iterative greedy activity selection algorithm has a running time of Ө(n). But the algorithm assumes that the activities are sorted by their finish times. If the activities are not sorted, how can we get the algorithm to work? What will be the new running time?

## Question 4
Discuss the difference/s between the greedy algorithm and the dynamic programming method with the help of the two versions of the knapsack problem. Include in your discussion how the greedy-choice property holds true only for one of the knapsack problems.

## Question 5 (programming)
The "non structural protein 2" (`nsp2`) protein is found to be linked to the mechanism of Coronavirus ([read more](https://onlinelibrary.wiley.com/doi/10.1002/jmv.25719)). Below is the sequence of this protein (first two lines, ignoring the line starting with a hash). In addition to the sequence of this protein, below are the sequences of two other similar (homologous) proteins (see [nsp2.hhba3m.txt](./nsp2.hhba3m.txt) for the alignment). Implement a dynamic programming solution to calculate the longest common subsequence (LCS) between - (a) `nsp2` and `A0A1B3Q5V8` and (b) `nsp2` and `Q9YMB7`. These are two problems that can be solved using the same implementation/code. Lower-case letters in the sequences, if there are any, must be skipped totally. You should print not just the length of the LCS but also the actual LCS.

## Question 6
When we use prefix codes to encode text, we can simply concatenate the codewords, i.e. we don't need a symbol to separate the codewords. Why doesn't this cause problems when decoding?

## Question 7
The table below represents two methods of encoding (fixed-length and variable-length). Discuss how the variable length encoding saves approximately 25% space.

Character |  a |  b |  c |  d |  e |  f 
-- | -- | -- | -- | -- | -- | -- 
Frequency | 45 | 13 | 12 | 16 | 9 | 5
Fixed-lenth codeword | 000 | 001 | 010 | 011 | 100 | 101
Variable-length codeword |  0 |  101 | 100 | 111 | 1101 | 1100

## Question 8
Create a string by concatenaring your first name, middle name and last name. Use the Huffman coding algorithm to create a codeword for each of the letter in your name. Start by creating a frequency table of letters such that the characters are ordered by their frequency. Most importantly, show the steps of the Huffman's algorithm by displaying how the Huffman (binary) tree grows after each step.

## Question 9 
What is the optimal Huffman code for the following set of frequencies, based on the first n Fibonacci numbers? show the steps of the Huffman's algorithm by displaying how the Huffman (binary) tree grows after each step. Optionally, you can also use the Python code below to verify your answer. (from CLRS 16.3-3)
```
a:1 b:1 c:2 d:3 e:5 f:8 g:13 h:21
```

## Question 10 (programming)
Compress [reddit_relationshipadvice_legaladvice_2000.txt](./reddit_relationshipadvice_legaladvice_2000.txt) using the Huffman's algorithm implemented below. Extend the code to read the file and write the compressed file. How will you verify that the codewords make sense?

----
# Python implementation of the Huffman's algorithm 
```python
import heapq

def huffman_encode(frequency):
    heap = [[weight, [symbol, '']] for symbol, weight in frequency.items()]
    heapq.heapify(heap)
    while len(heap) > 1:
        lo = heapq.heappop(heap)
        hi = heapq.heappop(heap)
        for pair in lo[1:]:
            pair[1] = '0' + pair[1]
        for pair in hi[1:]:
            pair[1] = '1' + pair[1]
        heapq.heappush(heap, [lo[0] + hi[0]] + lo[1:] + hi[1:])
    return sorted(heapq.heappop(heap)[1:], key=lambda p: (len(p[-1]), p))

data = 'aaccbaaaaaaaaddaaabdebacbaafabaadaaadacabdaefcaaeeaabfdcaaecbbbadafeaaaadadfbdcdabdeccdcadaadbaeaaec'
print('Data:')
print(data)

from collections import defaultdict
frequency = defaultdict(int)

for symbol in data:
    frequency[symbol] += 1

print('')
print('Symbol frequencies:')
print(frequency)

huff = huffman_encode(frequency)

print('')
print('Huffman codes:')
for p in huff:
    print (p[0], str(frequency[p[0]]), p[1])
```
```
Data:
aaccbaaaaaaaaddaaabdebacbaafabaadaaadacabdaefcaaeeaabfdcaaecbbbadafeaaaadadfbdcdabdeccdcadaadbaeaaec

Symbol frequencies:
defaultdict(<class 'int'>, {'a': 45, 'c': 12, 'b': 13, 'd': 16, 'e': 9, 'f': 5})

Huffman codes:
a 45 0
b 13 101
c 12 100
d 16 111
e 9 1101
f 5 1100
```

## Optional Question (not for bonus points)
Discuss how the activity selection problem exhibits the optimal substructure property.

