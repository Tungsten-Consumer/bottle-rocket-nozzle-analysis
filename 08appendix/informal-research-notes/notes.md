5.1 Mesh Description

* openfoam turns a shape into discreet "cells"
* cells are basically a 2d polygon facing any direction in 3d space
* the points on a cell are described by one vector per point, and the face can be described with the normal vector (showing its direction)
* an edge is the line between two points of a cell
* edges must be used by exactly two faces of a cell, all the normal face vectors must sum to zero, and cannot overlap



5.3 Mesh boundary

* i think this is for approximation of sine boundaries or other weird geometry restrictions, i think i can skip it because i want a box boundary



5.4 blockMesh

* i can describe vertices using a list called "vertices" with three numbers per entry (x y z), with each point in the list having its own index number
* convertToMeters is a conversion factor for all the numbers (value 0.001 = mm, value 1 = m)
* you can define edges with arcs and other shapes, but i want a giant cube, so i can ignore this or only use "line"
* blocks can be defined using the vertex numbers, the amount of cells in each firection, and the cell expansion ratios



5.5 snappyHexMesh

* i think i just need to find a tutorial file, then copy and modify it to get my new file that can be used
* I just realized that the user guide does not say how use snappyhexmesh, just how it works and what the parameters mean
* the file just has the generation params, which i will not touch for now
* insidepoint needs to be inbetween the boundaries of the fluid and the object
* 





