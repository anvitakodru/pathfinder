## A Star Path Finder - Microsoft Codess Mentorship, 2020

### Introduction
The aim of this project is to provide a path-finding library to approximate the shortest path in real-life situations, like- in maps, games where there can be many hindrances. I've considered a 2D Grid having several obstacles genearted randomly and we start from a source cell (top left corner of the grid) to reach towards a goal cell (bottom right corner). This project is made using the _p5.js library._
### The A* algorithm
A* Search algorithm is indeed a well known technique used in path-finding and graph traversals. Consider a square network/grid that has obstacles and we are given a start cell and a target cell. Our job is to reach the target cell (if possible) from the start cell as efficiently possible in the shortest path. 

The A* Search Algorithm, selects the node based on a value 'f', which is equal to the summation of two other values, 'g' and 'h'. At each succession, node/cell with the smallest ‘f’ value is selected, and processed.

We define ‘g’ and ‘h’ as follows:

g = the movement cost to move from the start cell to a given square on the network, following the path initiated to get there.

h = the estimated movement cost to move from that given square on the grid to the final target. This is known as the heuristic: a kind of smart guess. The actual distance isn't known until we path is found. There are several ways to calculate this ‘h’.
### Heuristics
h can be calculated in 2 methods:
* `Calculate the exact h value (very time consuming).` 

                            (or)
                            
* `Approximate the h value with the help of heuristic methods (less time consuming).`

**1) Exact Heuristics –**

A few methods to calculate the exact value of h are as follows:

(i) Pre-compute the distance between each pair of cells prior to the running of the A* Search Algorithm.

(ii) If there are no deterrents, at that point, the specific estimation of h can be found with no pre-calculation utilizing the formula of Euclidean Distance.

**2) Approximation Heuristics –**

There are generally three approximation heuristics to calculate h, namely, _Manhattan Distance, Diagonal Distance_ and thirdly _Euclidean distance._ We've implemented the heuristics using the **Euclidean Distance** method and the same is explained below.

• h is the distance between the current cell and the target cell computed using the distance formula:
   
   `h = sqrt ( (current_cell.x – target.x)2 + 
            (current_cell.y – target.y)2 )` 
            
• This heuristic is used when we are allowed to move in any direction, inclusive of diagonal movement.



