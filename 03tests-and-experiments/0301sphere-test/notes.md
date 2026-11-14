objective: calculate the drag coefficient of a sphere and compare it to cited numbers

software: freecad and openfoam v13

sphere is 1 cm radius

fluid domain is a 50x50x50cm box



* made a sphere in freecad
* made a copy of a tutorial file (the cylinder file) and put it into a new project directory
* imported the .obj export (with parameterized surface, in mm) into the copy of the tutorial file, and made the triSurface file
* made copies of the blockMesh and the snappyHexMesh tutorial files (both were called pipe or something similar), and placed them into the project directory
* took the missing system files (that was found within the snappyHexMesh) and pasted them into the system file of the original tutorial file (now renamed sphere-sim)
* modified blockMeshDict to be a cube that was 50cm x 50cm x 50cm, and added the 3d parameters for Aref and diameter
* made the inlets and the outlets allow flow across the +x direction
* modified snappyHexMeshDict to reference sphere.obj, with scale 0.001mm because of the .obj save settings, and slightly higher cell resolution
* removed features content and refinement regions within snappyHexMeshDict because they referenced seemingly random files, so i deleted the contents beauce they caused problems (command wont run)
* loop of doing 'blockMesh' and 'snappyHexMesh -overwrite' and debugging
* finally have proper meshes that are okay (after using checkMesh)



* now to run the simulation 
* 

