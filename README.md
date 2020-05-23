# Spring-2020-ITCS-8150-IntelligentSystems
This repository contains the projects and assignments of course "ITCS 6150/8150: Intelligent Systems". This course has been taken in Spring 2020 semester, as part of my PhD degree at UNC Charlotte.

## Git Clone Instruction
This repository uses `Git submodules` to manage external dependencies. Hence, please specify the `--recursive` option while cloning the repo as follow:
```
git clone --recurse-submodules https://github.com/biqar/Spring-2020-ITCS-8150-IntelligentSystems.git
```
## [Project 1: Solving 8-puzzle using A* search algorithm](https://github.com/biqar/puzzle-solver/tree/master/src/8-puzzle)

You are to implement `A*` search algorithm and apply it to `8-puzzle` problem, using any programming language 
of your choice.

In addition to coding of `A*` search algorithm, provide state space representation, operators, `g` (cost) and 
two heuristic functions of the `8-puzzle` problem. Your program should accept initial and goal states from 
user and will compute the best path. You will turn in the following as hard copy directly to me in the class, 
in addition to submitting everything in canvas:

* A report covering `8-puzzle` problem formulation, program structure, global variables, functions and procedures, etc. [10 points]
* Analyze six input/output cases:
   * For each input/output sample, for each heuristic report the following: (1) The solution path from initial state to goal state (2) the number of nodes generated, and (3) the number of nodes expanded.
      * For each heuristic (6 x (1.5 + 1.5 + 1.5)) = 27 points
      * Total 54 points [27 + 27]
   * Summarize the results in a table. [6 points]
* Error free source code with adequate inline documentation.
* Quality of the report and code (e.g. taking user input) [5 points]

### Sample initial and goal states
```
Initial state:             Goal State:
1 2 3                      1 2 3
7 4 5                      8 6 4
6 8 0                      7 5 0

Initial state:             Goal State:
2 8 1                      3 2 1
3 4 6                      8 0 4
7 5 0                      7 5 6
   
Initial state:             Goal State:
7 2 4                      1 2 3
5   6                      4 5 6
8 3 1                      7 8
```

## [Project 2: Solving N-queens problem using hill-climbing and its variants](https://github.com/biqar/puzzle-solver/blob/master/src/n-queens)

You are to solve the `n-queens` problem by using `hill-climbing` search and its variants. Read the slides or textbook carefully for the basic `hill-climbing` algorithm as applied to the `8-queens` problem. However, your program should treat the number of queens as a variable `n` and allows the user to input the value of `n`. Using any programming language of your choice, implement the followings:

* Hill climbing search (slides 9 - 10, 22)
* Hill-climbing search with sideways move (slides 23 and 24)
* Random-restart hill-climbing with and without sideways move (slides 28 -30)

Your program should report the following with respect to the 8-queens problem
1. Implement Hill climbing search
   * Run several times, say 100 to 500, and report success and failure rates
   * The average number of steps when it succeeds
   * The average number of steps when it fails
   * The search sequences from four random initial configurations
2. Hill-climbing search with sideways move
   * Run several times, say 100 to 500, and report success and failure rates
   * The average number of steps when it succeeds
   * The average number of steps when it fails
   * The search sequences from four random initial configurations
3. Random-restart hill-climbing search
   * The average number of random restarts required without sideways move
   * The average number of steps required without sideways move
   * The average number of random restarts used with sideways move
   * The average number of steps required with sideways move

Your program should be well documented, and you should turn in the following in **hard copy**:
1. An external documentation describing the n-queens formulation, the program structure, global variables, the function/procedure to compute the heuristic function, and other functions/procedures,
etc.
2. Your program source codes (with necessary inline documentation);
3. The execution results as specified above.

**In addition, each member should also upload everything (e.g. report, code, etc.) to Canvas.**

**Warning:** Any form of cheating will subject you to severe disciplinary act.

## [Project 3: Constraint satisfaction problems (CSP) - Map Coloring](https://github.com/biqar/puzzle-solver/tree/master/src/k-coloring)

A `K-coloring` of a map is an assignment of `K` colors, one to each country, in such a way that no 
two countries sharing a border have the same color. This problem can be translated to a constraint graph. 
A coloring of a graph G assigns a color to each vertex of `G`, with the restriction that two adjacent 
vertices never have the same color. The chromatic number of `G`, written `χ(G)`, is the smallest number 
of colors needed to color `G`. 

In this project, we will experiment with map coloring techniques and compare the observed results in 
the context of `USA` and `Australia` maps. 

* Compute the chromatic number of USA and Australia map. 
* Experiment with both maps using the following methods [`without heuristics`]
    * Depth first search only 
    * Depth first search + forward checking
    * Depth first search + forward checking + propagation through singleton domains
* Experiment with both maps using the following methods `with heuristics` where the order of variables needs to be defined in the following order `MRV`, `Degree Constraint`, and `Least Constraining Value`
    * Depth first search only 
    * Depth first search + forward checking
    * Depth first search + forward checking + propagation through singleton domains
* Present the results in a tabular format
    * the number of backtracking happened and
    * the time required to compute the result.

### General instructions:

1. The project can be completed individually, or in a group of three max. 
    * Many students work alone, which is good. If you prefer to work in a group, you are responsible for making your own group. 
    * You can try here (Links to an external site.).  
2. Map visualization is preferred but not required.  For visualization you can use any framework or tool.

### Submission instructions:

1. Your program should be well documented, and you should turn in the following to canvas.
    * An external document describing the map coloring problem formulation, the program structure, global variables, the function/procedure to compute the heuristic function, and other functions/procedures, etc.
    * Your program source codes (with necessary inline documentation);
    * The execution results as specified above.
    * Each member must turn in everything in canvas.
2. 10% late submission penalty for each extra day. Cut-off: Three days after the deadline.

**Warning:** Any form of cheating will subject you to disciplinary act.

### Guideline for Experiments:
Here is a guideline to experiment with map coloring algorithms.

#### Without Heuristics
1. Define the order of states randomly for map coloring
2. Run the following algorithms for the same random order of states
    * Depth first search only 
    * Depth first search + forward checking
    * Depth first search + forward checking + propagation through singleton domain
3. Repeat steps 1 and 2 at least four times. 
4. Show the results in a table for both maps

#### With Heuristics
1. Start with a state 
2. Run the following algorithms - this time, you will use heuristics to select next variable and value where appropriate at runtime
    * Depth first search only 
    * Depth first search + forward checking
    * Depth first search + forward checking + propagation through singleton domain
3. Repeat steps 1 and 2 at least four times. 
4. Show the results in a table for both maps

Compare all results and analyze them. 

## Resources
1. [Book] Artificial Intelligence: Foundations of Computational Agents: https://artint.info/2e/index.html
