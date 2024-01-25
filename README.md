This is a basic case setup for a water droplet falling into a water basin.

To run the simulation, run the Allrun script by typing

./Allrun &

in the terminal.

See Allrun script for details about what it does.

Simulation can be killed by first typing "jobs" in the terminal, reading the job
number of "Allrun" and then typing "kill %3" if the job number is 3.

To clean the case after running it, run the Allclean script.

Gravity is set in constant/g.

Fluid visocsity and surface tension are set in constant/transportProperties.

Initial water surface height and spherical droplet position and radius are set
in system/setAlphaFieldDict.

Initial droplet velocity is set in system/setFieldsDict.

To inspect the results in paraview, open paraview, go to File->Load State and 
then choose the file called state.pvsm. You may need to press the "..." next to 
"File Name" in the Properties tab ofthe Pipeline Browser and choose the file
called baseCase.foam in the case directory.

To change the mesh resolution and domain size you must modify the 
system/blockMeshDict file, but note that if you go above a couple of tens of 
thousands of cells (nCells = nx*ny*nz) the simulation may become very slow.

If you want to try to run the case in parallel, then you shouldgo to the Allrun
script and comment out "runApplication $(getApplication)" and remove the 
comments from the lines

#runParallel $(getApplication)
#runApplication decomposePar

You choose the number of cores (CPUs) in system/decomposeParDict. Note that you
should not run on more cores than you have physical CPU's on your computer.
Also pay attention to the total size of the data you write out, since it may
fill up your harddisk. To view a parallel simulation in paraview, open the
state.pvsm file from paraview, but under "Case Type" selecet "Decomposed case"
instead of "Reconstructed Case".