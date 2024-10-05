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
