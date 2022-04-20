# Extra Credit 2

Solve the following problem. Write up a paragraph explaining your thought process to solving this problem.

Write a function that takes in a non-empty array of arbitrary intervals,
merges any overlapping intervals, and returns the new intervals in no
particular order.

Each interval <span>interval</span> is an array of two integers, with
<span>interval[0]</span> as the start of the interval and
<span>interval[1]</span> as the end of the interval.

Note that back-to-back intervals aren't considered to be overlapping. For
example, <span>[1, 5]</span..


Also note that the start of any particular interval will always be less than
or equal to the end of that interval.


intervals =  = [[1, 2], [3, 5], [4, 7], [6, 8], [9, 10]]

Sample output should be:
[[1, 2], [3, 8], [9, 10]]

// Merge the intervals [3, 5], [4, 7], and [6, 8].
// The intervals could be ordered differently.
