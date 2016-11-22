# CSCI233-last-lab
Last 232 lab of the semester, we hope.

Lab4 (due 12/9)
In describing and analyzing Strassen's algorithm we assumed that we used divide and
conquer all the way down to tiny matrices. However, on small matrices the ordinary bruteforce
matrix multiplication algorithm will be faster because of lower overhead. This is a
common issue with divide and conquer algorithms. The best way to run these algorithms
is to test the input size n at the start to see if it is big enough to make using divide and
conquer worthwhile; if n is larger than some threshold then the algorithm would do a level
of recursion, if n is below that threshold then it would do the non-recursive algorithm. Your
job is to figure out the best choice for that threshold value for a version of Strassen's
algorithm based on your implementation. (See the class slides for the description of the
Strassen's algorithm and for the code for the basic non-recursive algorithm for matrix
multiplication.)
Steps:
1. First, write a function that implements the ordinary brute-force algorithm for matrix
multiplication over the integers (see the slides).
2. Next, write a recursive function that implements Strassen's algorithm for matrix
multiplication over the integers (see the slides). To keep the recursion simple, you
can assume that the input matrices are nxn matrices where n is a perfect power of
2.
3. Now modify your recursive function so that it uses an extra argument s and tests
the input size n of the matrices first. If n is at most s then it skips out of the recursion
and calls the brute-force version from above.
4. Your job now is to figure out which value of s is best to use with your algorithm.
To do so, you will need to figure out how long your code takes to work for various
values of s.
(You can assume s is a power of 2. You can experiment with n = 2048)
You are required to upload a write-up (a pdf) to D2L. Your write-up should include
 your code
 specification of your system (in a table, see below)
 the timings that you found (a table and a plot, see below)
 and the choice of s you found works best
Upload only your write-up which includes your code. Do not upload the actual .java
file.
Use a table like following to list the details of your system.
Table 1: Specification of the environment.
Processor Speed
No. of cores
Size of Memory
Operating System
Programing language
Use a table like the following to report your timings. Calculate average time over at least
10 runs on random matrices for each n.
Table 2: Running times for various s.
s Avg. running time (seconds)
2
4
8
Then plot the above values in a 2-D line chart in which x-axis is s and y-axis is time
(seconds) as shown below. Make sure to include a caption, axis labels and tick labels.
Figure 1: Variation of running time with s.
(10 Bonus points) Generalize your code so that it works with matrices of any dimension,
not just powers of 2. Figure out the best value of s to use in this case by re-doing the above
analysis.
0
1
2
3
4
5
2 4 8
Running time (seconds)
s
