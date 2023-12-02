# DL_Project_-Ojasvi-Shrivastava-
Hello Everyone & Welcome to Ojasvi Shrivastava's CS 131 Presentation

# Dynamic Programming

# Knapsack Problem 
Initialize the dynamic programming table:

Create a 2D table dp with dimensions (n+1) x (capacity+1), where n is the number of items and capacity is the maximum weight constraint.
Initialize all elements of the table to 0.
Fill the dynamic programming table:

Iterate through the items in order (from index 1 to n).
For each item, iterate through all possible weights (from 1 to capacity).
Check if the current item's weight is greater than the current weight.
If so, the maximum value for this weight remains the same as the previous item.
Otherwise, calculate the maximum value for this weight considering both including and excluding the current item:
Maximum value without the current item: dp[i - 1][w]
Maximum value with the current item: item.value + dp[i - 1][w - item.weight]
Choose the maximum value between including and excluding the current item and store it in dp[i][w].
Find the maximum value:

After filling the table, the maximum value for the knapsack problem can be found at dp[n][capacity].
This code efficiently solves the knapsack problem by storing the intermediate results in the dynamic programming table, avoiding redundant calculations and improving the overall time complexity.
