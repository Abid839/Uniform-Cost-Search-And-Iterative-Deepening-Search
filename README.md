# Uniform-Cost-Search-And-Iterative-Deepening-Search

# 1. # Uniform Cost Search

a. Overview:

Uniform Cost Search is a fundamental algorithm in the field of artificial intelligence and graph theory. It guarantees to find the solution with the minimum cost in a weighted graph. In this implementation, the algorithm is applied to the 8-puzzle problem, a sliding puzzle that consists of a 3x3 grid with 8 numbered tiles and an empty space.

b. Algorithm Details

The Uniform Cost Search algorithm works as follows:

    Initialize a priority queue with the start state and cost 0.
    While the priority queue is not empty:
        Dequeue the state with the lowest cost from the priority queue.
        If the state is the goal state, the algorithm terminates, and the solution is found.
        Otherwise, generate successor states, calculate their costs, and enqueue them into the priority queue.
    If the priority queue becomes empty and the goal state is not reached, there is no solution for the given problem instance.

c. Example

Start state:
[2, 1, 6]
[3, 4, 8]
[5, 7, 0]

Step 0:
[2, 1, 6]
[3, 4, 8]
[5, 0, 7]

Step 1:
[2, 1, 6]
[3, 0, 8]
[5, 4, 7]

Step 2:
[2, 1, 6]
[3, 8, 0]
[5, 4, 7]

Step 3:
[2, 1, 6]
[3, 8, 7]
[5, 4, 0]

Step 4:
[2, 1, 6]
[3, 8, 7]
[5, 0, 4]

Step 5:
[2, 1, 6]
[3, 0, 7]
[5, 8, 4]

Step 6:
[2, 1, 6]
[3, 7, 0]
[5, 8, 4]

Step 7:
[2, 1, 6]
[3, 7, 4]
[5, 8, 0]

Step 8:
[2, 1, 6]
[3, 7, 4]
[5, 0, 8]

Step 9:
[2, 1, 6]
[3, 0, 4]
[5, 7, 8]

Step 10:
[2, 1, 6]
[3, 4, 0]
[5, 7, 8]

Step 11:
[2, 1, 0]
[3, 4, 6]
[5, 7, 8]

Solution found!
Number of steps: 11
Total states generated: 189
