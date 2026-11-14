I see that you have clicked onto the project lore. Wise choice. This serves as an informal journal detailing everything I feel like writing down. This will genuinely be a heterogenous and highly viscous liquid in a deep pot, served on a rusty plate via soup ladle. In other words, this will be slop, in all that the word entails. Have fun reading this. There will be no grammar or spelling conventions from here on.



**2026-11-10 (Day 1)**

day one, brick by brick.



learnt the basics of GitHub. i must later fill in formal descriptions of all the files within the README.md: make them short and concise, as i will make them more substantial when necessary.



i must start learning how to use openFOAM, pick a cad software (like fusion or onshape or blender), and an analysis software (probably open source like wolfram, or something like MATLAB that is paid), and continue learning math and physics, as i need pdes to understand openFOAM, and i need knowledge and intuition of fluid dynamics to explain what is going on. i must also balance schoolwork and extracurriculars like sat and ap, while maintaining regular commitments to this.



i also need to write down everything from math and physics that is relevant to this, like the simplified navier stokes, drag (pde), mass flow rate, vector calc operations (div, curl, laplacian), theorems (greens stokes gauss), fourier, taylor, regular calc, multivariable calc, odes (separable, eulers, laplace transforms) etc. etc.





**2026-11-11 (Day 2)**

i got a lil bit done i guess. nothing really of note happened today.

other than realizing the superiority of .md files over .txt files for formatting withing GitHub, dayum it looks so much better, it isn't a pain to scroll to the side anymore



i now know how openfoam works i think. i think what it does is it takes your cad file (bottle rocket model) it slices it into discreet planes, only the surface though, because the volume is irrelevant. it then calculates tensors (by setting boundary conditions and initial conditions: like velocity of the gas, viscosity, and other variables) and sums them up and creates a small dt (delta time) with the sum of forces, then continues on after, creating small finite frames of time. after the simulation, it can either empirically tell me the drag coefficient, or even better, tell me the drag force itself over time based off its trajectory or something (i haven't a clue, this is just my intuition), then i can plug in the data using a simple script on MATLAB or some other software and get my predicted trajectory.



I also need to use simplefoam or whatever its called because i need incompressible flow that is also turbulent



i also heard from my science teacher that navier stokes are an utter pain in the rear to solve by hand, so i aint doing that, hence openfoam and using the incompressible simplified version (because water and compressed air is practically incompressible flow)



i will need to learn more about the formulas required to undertake this project, and list them within the reference sheet before i create my hypothesis. i should also create test cfd files and test openfoam simulations to figure out how the tool works. i will also have to see if i can procure a student licence for matlab if such a liscence exists, preferably if it was free.



ALWAYS USE MD FILES FOR ACTAL PARAGRAPHS AND STUFF FROM NOW ON



matlab may be out of my budget range.



scilab, Julia, python, gnuoctave may be alternatives





**2026-11-13 (Day 3)**

attempting openfoam tests on a sphere, then deriving the drag coefficient, then comparing it to someone else's result... sounds like an incredible plan



i have written down what i think i need to know to generate more meshes for future attempts, as ill need many meshes for nozzle simulations. i also now know that blockMesh needs to be created using coding, as it is simple to define a cube, and the boundaries (because boundaries do not need to be complex). snappyHexMesh needs an .obj file, and takes a few minutes to generate a polyMesh file. i now need to change the actual setup conditions with the files physicalProperties, momentumTransport, 0/U, 0/p, system/controlDict, system/fvSchemes, system/fvSolution, system/forceCoeffsIncompressible; and then i need to format the other 0 files for turbulence, like 0/k, 0/omega, 0/epsilon, and 0/nut.



debugging the blockMeshDict and the snappyHexMeshDict was a bit of a pain, but that is to be expected. ill also have to read more of the openfoam v13 user manual to find the stuff that is needed to be modified for these files. i will also have to learn more equations, like the viscosity equations, what the Reynolds number is used for, and the variables in the drag equation, so i can later sub in them onve i obtain the drag force for my sphere.



doing this also gives me a reusable framework for the actual bottle rocket, and it's drag, plus it will later give me some initial conditions to actually run some more simulations on nozzles and bottle rockets with potentially oblique directions, and it will give me understanding of the OpenFOAM machinery, allowing my to simulate actual thrust of the bottle rocket, and using both the thrust and the drag forces to plot a trajectory on jupyterlab and python.



oh yeah and use 'cd \~/openfoam-cases/sphere/sphere-sim' on ubuntu to get right back to the proper directory

