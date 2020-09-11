# Homework 2

# Read section 15.1 from CLRS
Please read this with the goal of using the knowledge to do the homework below.

# Watch the recorded lectures
- [The rod cutting problem explained](https://youtu.be/mOFHQ1kUIpk)
- [Recursive solution to the rod cutting problem](https://youtu.be/2pnCqUz17cQ)
- [What is dynamic programming? Intuition of dynamic programming](https://youtu.be/D3hSqIQv5Hg)
- [Dynamic programming for solving the rod cutting problem](https://youtu.be/L9Y1pqtptPE)

# Question 1
Create your own length-price table consisting of at least six length-price pairs and with the help of this table explain the rod cutting problem ***in your own words***.

# Question 2
Change the following recursive implementation to solve the rod cutting algorithm so it also prints where to make the cuts. Do not convert it to the memoized version, just extend this to print where to make the cuts. Verify your answer by checking if the optimal cuts suggested by your program actually result in maximum revenue.

```python
# Recursive solution to the rod-cutting problem (top-down approach)
import sys
#p = (-1000, 1,5,8,9,10,17,17,20,24,30)
p = (-1000, 1,5,8,9,10,17,17,20,24,30, 32, 34, 36, 38, 40, 42, 44, 46, 48, 50, 52, 54, 56, 58, 60, 62, 64, 66, 68)

def CUT_ROD(p, n):
      if n == 0:
            return 0
      q = -1000000
      for i in range(1, n+1):
            q = max(q, p[i] + CUT_ROD(p, n-i))
      return q

print ("")
print ("L = " + str(len(p)))

print ("")
for i in range(1, len(p)):
      sys.stdout.flush()
      print (str(i) + " (p="+str(p[i])+") => " + str(CUT_ROD(p, i)))
```

# Question 3
Discuss why the recursive solution to the rod cutting problem is so inefficient?

# Question 4
Discuss the two dynamic programing approaches. If you were asked to implement, which one would you choose, and why?

# Question 5
Comapare and discuss the running times of a recursive solution (without memoization) and a the dynamic programming solution to the rod curring problem.
