# Uniform-Cost-Search-And-Iterative-Deepening-Search

# 1.  Uniform Cost Search

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



# 2. 8-Puzzle Solver using Iterative Deepening Search
This repository contains Python code to solve the 8-puzzle problem using Iterative Deepening Search (IDS). The 8-puzzle is a sliding puzzle that consists of a 3x3 grid with 8 numbered tiles and a blank space. The goal of the puzzle is to rearrange the tiles from a given initial state to the goal state:

**Goal state:**

1 2 3

4 5 6

7 8 0


### Here's how IDS works:

Depth-First Search (DFS): DFS explores as far as possible along each branch before backtracking. It can get stuck in deep branches, especially if the goal is located in a shallow branch.

Breadth-First Search (BFS): BFS explores all the neighbor nodes at the present depth before moving to nodes at the next depth level. It ensures that the shallowest nodes are visited first. However, it requires a lot of memory to keep track of all the nodes at the current depth level.

Iterative Deepening Search combines these two approaches:

Depth-Limited Search: It starts with a depth limit of 0 and performs DFS up to that limit.

Increase Depth Limit: If the goal node is not found within the depth limit, increase the limit by 1 and perform DFS again.

Repeat: Repeat this process until the goal node is found.

The key idea is that IDS combines the memory efficiency of DFS and the completeness of BFS. It explores the search space incrementally, starting from a depth of 0 and gradually increasing the depth limit until the solution is found. It's guaranteed to find the solution if the branching factor is finite and the cost function is non-decreasing with respect to the depth of the node.

However, IDS can be inefficient in terms of time complexity because it repeatedly explores nodes at the earlier depth levels. Still, it's often preferred when the depth of the solution is unknown and the search space is not exceedingly large, as it uses less memory compared to BFS.

### Start state:
2 1 6

3 4 8

5 7 0

step-1

[2, 1, 6]

[3, 4, 8]

[5, 7, 0]

step-2

[2, 1, 6]

[3, 4, 0]

[5, 7, 8]

step-3

[2, 1, 0]

[3, 4, 6]

[5, 7, 8]

step-4

[2, 0, 1]

[3, 4, 6]

[5, 7, 8]

step-5

[0, 2, 1]

[3, 4, 6]

[5, 7, 8]

step-6

[3, 2, 1]

[0, 4, 6]

[5, 7, 8]

step-7

[3, 2, 1]

[5, 4, 6]

[0, 7, 8]

step-8

[3, 2, 1]

[5, 4, 6]

[7, 0, 8]

step-9

[3, 2, 1]

[5, 4, 6]

[7, 8, 0]

Solution found:
Number of steps: 8
Total states explored: 272
