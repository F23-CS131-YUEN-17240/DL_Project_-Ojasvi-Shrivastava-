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

# Shortest Path Problem
Initialize distances:

Create a list distances of length equal to the number of nodes, initialized with infinity for all nodes and 0 for the source node.
Initialize unvisited set:

Create a set unvisited containing all nodes.
Iterate until unvisited set is empty:

While unvisited:
Find the unvisited node with the minimum tentative distance.
Remove the current node from unvisited.
Update distances for neighbors:

For each neighbor of the current node:
Update the neighbor's distance with the minimum of its current distance and the tentative distance through the current node.
Return distances:

Return the distances array containing the shortest distances from the source node to all other nodes.

# Game of Chess
The provided code defines a function evaluate_position() that assesses the strength of a chess position by calculating and combining material and positional values.

Material Value:

Determine the intrinsic value of pieces on the board based on their point values.
Positional Advantages:

Evaluate the strategic placement and interactions of pieces to assess their positional strength.
Combined Evaluation:

Combine material and positional values to obtain an overall evaluation score for the position.
Return Evaluation Score:

Return the evaluation score, indicating the perceived strength of the position.
