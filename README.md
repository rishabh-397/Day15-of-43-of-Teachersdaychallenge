# Day15-of-43-of-Teachersdaychallenge

A. Horseshoes
Problem Description: Valera has four horseshoes with colors s1, s2, s3, s4. He needs to wear four horseshoes of different colors. Determine the minimum number of horseshoes he needs to buy.

Key Idea/Logic:

The problem is equivalent to finding how many of the four given horseshoe colors are duplicates. The number of horseshoes to buy is 4 - (number of unique colors).

Approach:

Read the four integer color values s1, s2, s3, s4.

Store these four values in a set data structure. A set automatically stores only unique values.

The size of the set will give you the number of unique colors Valera already has.

Subtract the set's size from 4 to get the minimum number of horseshoes to buy.

Time Complexity: O(1) since the input size is fixed at 4.

Space Complexity: O(1) to store the set of colors.
Example:
Input: 1 7 3 3
Output: 1
Explanation: The unique colors are 1, 7, and 3. The set size is 3. 4 - 3 = 1. He needs to buy one more horseshoe.

A. Queue at the School
Problem Description: Given the initial arrangement of n boys ('B') and girls ('G') in a queue, and a time t in seconds, find the final arrangement. Each second, any boy standing immediately in front of a girl swaps places with her. All such swaps happen simultaneously.

Key Idea/Logic:

This is a simulation problem. You need to simulate the swapping process for t seconds.

Since multiple BG pairs can swap simultaneously, a single pass through the string for each second is needed.

Approach:

Loop t times (for each second).

Inside this loop, iterate through the queue from left to right.

Look for adjacent pairs of 'B' and 'G'.

If you find a 'B' at index i followed by a 'G' at index i+1, swap them.

Crucially, after swapping, you should skip the next position (i+1) in your inner loop to avoid re-evaluating the newly swapped pair in the same second, as swaps are simultaneous.

Time Complexity: O(N
cdotT) where N is the number of children and T is the number of seconds, as you iterate through the queue T times.

Space Complexity: O(N) to store the queue string/array.

Example:
Input:

5 2
BGGBG
Output: GGBGB
Explanation:

Initial: BGGBG

After 1s: GBGGB (B and G at pos 1,2 swap; B and G at pos 3,4 swap)

After 2s: GGBGB (B and G at pos 3,4 swap)

