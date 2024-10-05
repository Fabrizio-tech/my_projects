# my_projects
Repository containing some of my projects that I liked working on the most.

## Project 1:
### Name:           
**String Art**

### Language:       
**Python, PyTorch**

### Description:    
Image software in Python to generate wire art.  
The main idea is to transform a picture into art by drawing only with a continuous line between fixed nails in the frame.  
It optimizes the path using sparse matrix calculations, ensuring the wire covers the image's essential details.

### Current implementation:
- Generate circle with nails
- Start from a random nail and connect it with a wire to the nail that makes the path the most dark possible (avoid neighboring nails).
- From the current nail, compute the next one.

- To compute the best path: generate matrix of nails, indicates the avg color of the pixels in the path (values calculated in parallel).
  
### Current progress: 
- Made first version of the software
- images hard to see: change selection algorithm
- memory intensive
- relatively fast

## Project 2:
### Name:           
**Logistic Game of Life**

### Language:       
**Python, PyTorch**

### Description:    
Implementation of Logistic Game of Life: Game of Life is discrete, the logistic version allows for continuous values, inspired from a paper. 
Implemented also for High Life.

### Current implementation:
- Generate grid with random values of 0 and 1.
- Define rules of game of life, with an additional lambda parameter.
- Do the same for high life: study results.
- Interesting results at different lambdas show phase transformation.
  
### Current progress:
- implemented with torch: managed to optimize the speed of the simulation significantly
- computed several sims for to gain avg value
- at a specific lambda: the emergence of replicating patterns

## Project 3:
### Name:           
**2D realistic clouds**

### Language:       
**Python**

### Description:    
designed algorithm to generate 2D realistic-looking clouds. The main purpose is to use them in a 2D video game. 


### Current implementation:
- Generate grid of val 0 and a cell of val 1
- From the cell of val 1 generate another one in a random position, but not too far from prev one.
- Continue until multiple a generated
- Generate radii following a pawer law with lambda (1.2). As many points on the grid.
- Apply radii on points: generate circles of value one, when to circles overlap sum values
- Eliminate val 1 and 2
- Normalize grid
- Represent grid with: 0 in blue and 1 in white. The rest of the colors follow an S-shaped curve
  
### Current progress:
- effects very realistic, at different lambda different cloud types appear
- need to add shadows for more realistic effect

