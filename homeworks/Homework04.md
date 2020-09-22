# Homework 4

## Read sections 16.1 and 16.2 from CLRS
Please read this with the goal of using the knowledge to do the homework below.

## Watch the recorded lectures
1. [Why study greedy algorithms?](https://youtu.be/gHWxmb_nVpY)
1. [The activity selection problem for understanding greedy algorithms](https://youtu.be/tEfVXgrP6WU)
1. [Optimal substructure of the activity selection problem](https://youtu.be/LmlHHSr7gys)
1. [Intuition for understanding how greedy algorithms work](https://youtu.be/BWlXudP7Unk)
1. [Recursive greedy algorithm for the activity selection problem](https://youtu.be/alybycFq2mU)
1. [Iterative greedy approach to solve the activity selection problem](https://youtu.be/VPkTE5XoYQ0)
1. [Greedy algorithm vs dynamic programming]()

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

## Question 5 
To solve the activity selection problem, the technique of sorting activities by their number of overlaps and then selecting the activities that have minimum overlaps with other activities, does not work. Illustrate this with a simple example.

## Optional Question (not for bonus points)
Discuss how the activity selection problem exhibits the optimal substructure property.

