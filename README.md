# Implementation of RRT in python

### What is RRT?
- It is one of the various path planning algorithms. It’s a sampling-based algorithm that makes it very useful to plan high-dimensional robot paths.
- It starts with an empty tree. Then it generates random nodes in each iteration. Once a node is generated, it searches for an existing node present in the tree, which would have the minimum distance from that newly generated node. If there are no obstacles between the two nodes, a new edge is created between these two nodes and added to the tree. That’s how the tree expands and eventually finds its goal. Once the goal is reached, the path is shown between the starting node and the goal.


### Features of RRT
1. It doesn’t ensure an optimal path.
2. The growth of trees is heavily biased towards unexplored regions.
3. Using a growth factor restricts the chances of going too far in the wrong direction, making the path smoother.
4. The generation of a random state precisely at the position of the goal or final state is very unlikely. That’s why a predefined area around the final state is kept.
5. It is better than search-based algorithms like A* when dealing with high-dimension robots. 
6. Path found in RRT differs on average by a factor of 1.3 to 2.0 from the optimal path.
7. In the beginning, the tree expands non-uniformly to explore the four corners first. Once it’s achieved, the tree expands uniformly over the free space.
8. The generation of random vertices is independent of the position of the root vertex or starting point.
9. Once a tree is generated to find a goal state, we need not generate another new tree from scratch if the goal state position is changed, given that obstacles are not changing their position.



- Some snapshots:
![500](https://user-images.githubusercontent.com/97786651/209921161-c2db47db-5547-4d3a-bb33-ebe73147b229.png)
![1k](https://user-images.githubusercontent.com/97786651/209921212-e0d8a65e-e5fe-4748-93ac-a9cddef6797a.png)
![2k](https://user-images.githubusercontent.com/97786651/209921239-fa932c50-d596-4d63-8e62-f695d042242a.png)
